# postgres_docker_starter

### youtube guides
- [Learn how to use postgres sql with docker](https://www.youtube.com/watch?v=A8dErdDMqb0)
- [Docker with persistent storage](https://www.youtube.com/watch?v=G3gnMSyX-XM&t=1s)
- [Docker Volumes Setup](https://www.youtube.com/watch?v=G-5c25DYnfI)

## Agenda

### 1. Create a Postgres docker container
###### replace my_current_directory with your current directory
```bash
export MY_CURRENT_DIR=/Users/sayyidkhan/docker_volumes/pgdata;

docker run --name pgdata \
  -p 5432:5432 -d \
  -e POSTGRES_PASSWORD=password \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_DB=demo \
  -v $MY_CURRENT_DIR:/var/lib/postgresql/data \
  postgres
```

### 2. Connect and run some queries
#### connecting manually
```bash
docker exec -it pgdata psql -U postgres
```
#### Connecting using GUI
- download [dbeaver](https://dbeaver.io/download/)


| Syntax      | Info to Enter |
| ----------- | ------------- |
| Username    | postgres      |
| Password    | password      |
| Database    |stripe-example |
| Host        |localhost      |


<img width="600" alt="Screenshot 2021-10-04 at 3 56 18 PM" src="https://user-images.githubusercontent.com/22993048/135814703-e9031003-a9f2-4520-bb45-08add39538fb.png">

### 3. Automate - run scripts using docker CLI
###### sql script w/o using .sql file
```bash
docker exec -it pgdata psql -U postgres -f "$PWD/script_demo1.sql"
docker exec -it pgdata psql -U postgres -d demo -c "CREATE TABLE demo_db2(something int)";
docker exec -it pgdata psql -U postgres -d demo -f script_demo1.sql
```
