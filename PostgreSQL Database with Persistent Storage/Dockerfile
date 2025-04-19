FROM postgres:latest

ENV POSTGRES_USER=user
ENV POSTGRES_PASSWORD=password
ENV POSTGRES_DB=mydb

VOLUME ["/var/lib/postgresql/data"]
CMD ["postgres"]
EXPOSE 5432
# This Dockerfile sets up a PostgreSQL database with persistent storage.