FROM debian:bullseye

RUN apt update && apt install mariadb-server -y

COPY 50-server.cnf  /etc/mysql/mariadb.conf.d/.
COPY init.sql  /etc/mysql/init.sql
COPY script.sh  .

RUN chmod +x script.sh
RUN mkdir -p /run/mysqld

CMD ["./script.sh"]
