#

## MySQL

- docker run -p 3306:3306 --name=mysql-container --restart on-failure -d mysql/mysql-server:8.0
- docker logs mysql-container 2>&1 | grep GENERATED
  GENERATED ROOT PASSWORD: 5Fw:20?f/DO4yQ*aDp/+x7*R4OPT41J=
- docker exec -it mysql-container mysql -uroot -p
- ALTER USER 'root'@'localhost' IDENTIFIED BY 'root';
- update mysql.user set host = '%' where user='root';

### Connect from DBMS

- host: `0.0.0.0`
- port: `3306`

## Stack Overflow
https://stackoverflow.com/questions/33827342/how-to-connect-mysql-workbench-to-running-mysql-inside-docker
