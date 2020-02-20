

https://hub.docker.com/_/oracle-database-enterprise-edition

Oracle released  two official varients of OracleDB server edition docker images
        store/oracle/database-enterprise:12.2.0.1
        store/oracle/database-enterprise:12.2.0.1-slim



# How to pull oracle database image?

## Login to docker store
$ docker login

## pull Docker image from Docker store

$ docker pull store/oracle/database-enterprise:12.2.0.1


## Running oracle DB as container

$ docker run -d -it --name OracleDB -p 1521:1521/tcp -p 5500:5500/tcp store/oracle/database-enterprise:12.2.0.1


## Connecting to the Database Server

$ docker exec -it OracleDB bash -c "source /home/oracle/.bashrc; sqlplus /nolog"


## Connecting Database container from host machine 

$ sqlplus sys/Oradoc_db1@localhost:1521/ORCLCDB.localdomain as sysdba


We can create a user using following commands 

          connect sys as sysdba;
          -- Here enter the password as 'Oradoc_db1'
          create user user01 identified by user01;
          GRANT CONNECT, RESOURCE, DBA TO user01;

# connecting database from host machine

$ sqlplus user01/user01@localhost:1521/ORCLCDB.localdomain



Ref :
https://dzone.com/articles/oracle-12c-image-installation-in-docker


