FROM mysql:latest

LABEL database="studentapp"

ENV MYSQL_USERNAME="admin"
    MYSQL_ROOT_PASSWORD="admin1234"
    ENTRYPOINT="database-1.c10uu86mstml.eu-north-1.rds.amazonaws.com"

CMD mysql -h ${ENTRYPOINT} -U ${MYSQL_USERNAME} -p${MYSQL_ROOT_PASSWORD}

COPY init-db.sql /docker-entrypoint-initdb.d/

EXPOSE 3306

CMD ["mysqld"]
