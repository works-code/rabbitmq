# rabbitmq
##### # 개발 환경
- mac
- java 15
- rabbitmq client 5.10.0
- rabbitmq server ?
- spring boot
- gradle

##### # rabbitmq mac 설치
$ brew install rabbitmq

##### # rabbitmq start
$ /usr/local/sbin/rabbitmq-server

##### # rabbitmq manager ui
- http://localhost:15672
- 기본 계정 : guest / guest

##### # rabbitmq 계정 생성
$ /usr/local/sbin/rabbitmqctl add_user admin admin

##### # admin 권한 부여
$ /usr/local/sbin/rabbitmqctl set_user_tags admin administrator

##### # 계정 보기
$ /usr/local/sbin/rabbitmqctl list_users

##### # vhost 생성
$ /usr/local/sbin/rabbitmqctl add_vhost vhost-01

##### # 유저 vhost 권한 부여
예) rabbitmqctl list_permissions [-p vhost ] <user> <conf> <write> <read>
$ /usr/local/sbin/rabbitmqctl set_permissions -p vhost-01 admin ".*" ".*" ".*"
