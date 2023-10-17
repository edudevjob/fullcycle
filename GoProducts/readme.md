mysql> create table products (id varchar(255), name varchar(255), price float);
❯ docker-compose exec kafka bash
[appuser@kafka ~]$ kafka-topics --bootstrap-server=localhost:9092 --topic=product --create
Created topic product.
[appuser@kafka ~]$