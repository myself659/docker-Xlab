#https://hub.docker.com/r/mysql/mysql-server/tags
#docker pull mysql/mysql-server:5.7
FROM mysql:5.7

ENV MYSQL_DATABASE company

COPY  ./sql_scripts/  /docker-entrypoint-initdb.d/


