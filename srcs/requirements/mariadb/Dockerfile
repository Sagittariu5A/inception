FROM debian:buster

ARG MYSQL_DB_NAME MYSQL_USER MYSQL_PASSWORD

RUN apt update && apt install -y mariadb-server

COPY tools/setup.sh /tools/setup.sh

COPY tools/mysql.conf /etc/mysql/mariadb.conf.d/50-server.cnf

RUN chmod +x /tools/setup.sh && /tools/setup.sh

ENTRYPOINT [ "mysqld" ]
