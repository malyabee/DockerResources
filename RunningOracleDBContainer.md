

https://hub.docker.com/_/oracle-database-enterprise-edition

Oracle released  two official varients of OracleDB server edition docker images
        store/oracle/database-enterprise:12.2.0.1
        store/oracle/database-enterprise:12.2.0.1-slim



# How to pull oracle database image?

## Login to docker store
$ docker login

## pull Docker image from Docker store

$ docker pull store/oracle/database-enterprise:12.2.0.1


## Running oracle DB on server 

$ docker run -d -it --name Oracle-DB -p 1521:1521/tcp -p 5500:5500/tcp store/oracle/database-enterprise:12.2.0.1



