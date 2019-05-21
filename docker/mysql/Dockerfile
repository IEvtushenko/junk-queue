FROM mysql:8.0.15

RUN mkdir /var/log/mysql && chown -R mysql:mysql /var/log/mysql

VOLUME /var/log/mysql

COPY --chown=mysql:mysql my.cnf /etc/my.cnf

COPY --chown=mysql:mysql init.sh /docker-entrypoint-initdb.d/init.sh
RUN chmod +x /docker-entrypoint-initdb.d/init.sh

COPY entrypoint.sh /usr/local/bin/docker-entrypoint.sh
RUN chmod +x /usr/local/bin/docker-entrypoint.sh
