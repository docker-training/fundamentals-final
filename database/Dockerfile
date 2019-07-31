FROM postgres:9.6

ADD pg_hba.conf /usr/share/postgresql/9.6/
ADD postgresql.conf /usr/share/postgresql/9.6/

ADD init-db.sql /docker-entrypoint-initdb.d/

ENV POSTGRES_USER=gordonuser
ENV POSTGRES_DB=ddev
 
