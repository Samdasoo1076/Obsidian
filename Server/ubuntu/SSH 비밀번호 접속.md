sudo adduser -aG sudo 유저이름
sudo  adduser 유저이름
sudo passwd  유저 이름

sudo nano /etc/ssh/sshd_config.d/60-cloudimg-settings.conf
파일에서 no 에서 yes로 변경

sudo systemctl restart sshd