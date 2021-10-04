# postgres_docker_starter

[Learn how to use postgres sql with docker](https://www.youtube.com/watch?v=A8dErdDMqb0)
[Docker with persistent storage](https://www.youtube.com/watch?v=G3gnMSyX-XM&t=1s)

## Agenda

### 1. Create a Postgres docker container
```bash
docker run --name pgdata \
  -p 5432:532 -d \
  -e POSTGRES_PASSWORD=password \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_DB=stripe-example \
  -v pgdata:/var/lib/postgresql/data \
  postgres
```

### 2. Connect and run some queries
```bash
docker exec -it demo psql -U postgres
```
### 3. Automate - run scripts using docker CLI

## Connecting using GUI
- download [dbeaver](https://dbeaver.io/download/)
