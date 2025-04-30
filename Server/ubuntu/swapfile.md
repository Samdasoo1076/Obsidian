```bash
# 1. 현재 swap 해제
sudo swapoff -a

# 2. 기존 swapfile 제거 (존재할 경우)
sudo rm -f /swapfile

# 3. 4 GB 크기의 빈 파일 생성
sudo fallocate -l 4G /swapfile
# 만약 fallocate가 실패하면 아래 dd 명령 사용:
# sudo dd if=/dev/zero of=/swapfile bs=1M count=4096 status=progress

# 4. 권한 설정
sudo chmod 600 /swapfile

# 5. 스왑영역으로 초기화
sudo mkswap /swapfile

# 6. 즉시 활성화
sudo swapon /swapfile

# 7. 적용 확인
sudo swapon --show

# 8. 재부팅 후에도 자동으로 활성화되도록 fstab에 추가
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab

```