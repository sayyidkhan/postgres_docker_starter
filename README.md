# postgres_docker_starter

### youtube guides
- [Learn how to use postgres sql with docker](https://www.youtube.com/watch?v=A8dErdDMqb0)
- [Docker with persistent storage](https://www.youtube.com/watch?v=G3gnMSyX-XM&t=1s)

## Agenda

### 1. Create a Postgres docker container
```bash
docker run --name pgdata \
  -p 5432:5432 -d \
  -e POSTGRES_PASSWORD=password \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_DB=stripe-example \
  -v pgdata:/var/lib/postgresql/data \
  postgres
```

### 2. Connect and run some queries
#### connecting manually
```bash
docker exec -it pgdata psql -U postgres
```
#### Connecting using GUI
- download [dbeaver](https://dbeaver.io/download/)
- 


### 3. Automate - run scripts using docker CLI

