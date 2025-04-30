```bash
sudo apt update
sudo apt install apache2 -y // 아파치 설치 

sudo apt install software-properties-common -y  // 외부 apt를 받기 위해 필요한 ppa 저장소 관리 패키지
sudo add-apt-repository ppa:ondrej/php -y  //php 설치 
sudo apt update 
sudo apt install php8.2 libapache2-mod-php8.2 -y //php 관련 패키지 설치 

php -v // php 버전 확인 겸 설치 확인 

sudo systemctl restart apache2 // apahce 서버 재시작(php와 연동을 위해 )

echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/info.php
    // var/www/html 경로에 phpinfo(); 함수를 실행시킨 info.php 파일을 생성 

sudo apt update

sudo systemctl restart apache2

sudo a2enmod php8.2 // 시작 확인 
sudo systemctl restart apache2 // 서버 재시작 


cat /etc/apache2/mods-enabled/php8.2.conf //php 설정 파일 확인 

sudo systemctl start apache2 // 아파치 서버 시작 

sudo systemctl status apache2 // 아파치 서버 상태 확인

ip a // ip 확인
```


```bash
//mariadb 익스텐션 설치
sudo apt update
sudo apt install php8.2-mysql
sudo phpenmod mysqli
sudo systemctl restart apache2

.htaccess 활성화 방법

sudo a2enmod rewrite
/etc/apache2/apache2.conf 에서 
AllowOverride All 옵션으로 변경

```