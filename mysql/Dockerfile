FROM alpine:latest

RUN apk add --no-cache mariadb mariadb-client mariadb-server-utils

EXPOSE 3306

CMD ["mysqld", "--user=mysql", "--console"]