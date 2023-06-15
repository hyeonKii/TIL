1. 유저 접속
> mysql - u <user> -p

2. DB 생성
> create database <db-name>

3. DB 삭제
> drop database <db-name>

4. User 생성
> create user <user-name>@'host(ip)' identified by '<password>';

5. User 삭제
> drop user '<사용자>'@'host(ip)';

- 권한부여
grant all privileges on <db>.<특정 table or schema or procedure> to '<user-name>'@'host(ip)';

- 권한 적용
flush privileges

## Session의 개념
- 1개의 세션은 1개의 프로세스를 갖는다
- Tester라는 유저의 testdb로 mysql를 접속한다고 가정
  privileges를 체크하고 server socket port 3306으로 접속하게 된다
  mysql은 테이블(session id)을 하나 생성해서 character set, time stamp 정보를 갖는다
  mysql 상에서 작성한 쿼리문에 대한 결과값을 요청한 session id를 확인하고 전달한다

- 네이버 접속의 예
  내 컴퓨터로 네이버에 어떤 요청을 보냈다고 가정
  naver 서버에 session이 1개 생기고 서버에서 session id를 확인 후 응답을 전달한다.
  서버에서 session id를 클라이언트에게 전달한다.
  클라이언트는 받은 session id를 브라우저의 cookie에 심는다.