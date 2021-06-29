---
title: Postgres inside docker
date: "2015-05-01T22:12:03.284Z"
description: "Using the docker to quickly config the postgres database"
---

## Docker

Docker is containerized approach in the current web market, where we can deploy
out application on any cloud wihtout much effort. Most of cloub companies like AWS,
GCD, etc already have sevice for docker and container.

### What are container?

Container are virutal os inside main system as Virtual system but much fast and stable
compared to other VMs. Docker Image are the blueprint which is used to created the 
container, they are like the class (Image) and its object (Container).

## Postgres

Postgres is relation database used mostly these days. It's fast, efficient and developer friendly
I usually prefer postgres with respect to other dbs. There are other great alternatives as well
like Mysql and so on.

## Docker Compose

Docker compose allows to start multiple images/container in same instances and also allow communication
between them.

## Docker Compose for postgres with pg-admin interface

We are going to create the postgres docker compose file with pg-admin interface.

```yml
version: "3.8"
services:
  db:
    container_name: pg_container
    image: postgres
    restart: always
    environment:
      POSTGRES_USER: root
      POSTGRES_PASSWORD: root
      POSTGRES_DB: test_db
    ports:
      - "5432:5432"
    volumes:
      - ./postgres-data:/var/lib/postgresql/data
  pgadmin:
    container_name: pgadmin4_container
    image: dpage/pgadmin4
    restart: always
    environment:
      PGADMIN_DEFAULT_EMAIL: admin@admin.com
      PGADMIN_DEFAULT_PASSWORD: root
    ports:
      - "5050:80"
```
