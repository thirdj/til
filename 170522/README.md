## docker mariadb-utf8 설치

```
$ docker run -d --name mariadb-utf8 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=1111 aleksxp/docker-mariadb-utf8
// -d는 detach의 줄임말입니다. 컨테이너에 접속할 때 쓰였던 attach를 기억하시나요? -d 옵션을 사용하면 그 컨테이너는 detach되어 attach 하지 못합니다. 즉 컨테이너에 접속하지 못한다는 말이지요. 알아가도록 합시다. -d 옵션을 준 컨테이너는 attach 하지 못합니다.

$ docker exec -i -t mariadb-utf8 bash
// exec 명령에서 -i -t 옵션을 준 이유는, bash를 사용해도 interactive 하게 터미널처럼 사용하기 위해서 사용한것
```