#2024-11-12 #2024-11 #2024- [[2024-11-12 회사]] [[2024-11-12 플젝]] [[서버 구성]]
#회사 #프로젝트

## 메모
원초적인 디버깅(에러찾기는)
```linux
sudo tail /var/log/apache2/error.log
```

화면에 오류 출력 
apahce2 / php.ini에서 
display_errors = On
display_startup_errors_ On

apache2 / php_ini에서 
short_open_tag = On

