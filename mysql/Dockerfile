FROM mysql:5

RUN rm -Rf /etc/mysql/mysql.conf.d && \
    mkdir /etc/mysql/mysql.conf.d

COPY db-schema.sql /docker-entrypoint-initdb.d
COPY my.cnf /etc/mysql/my.cnf


EXPOSE 3306