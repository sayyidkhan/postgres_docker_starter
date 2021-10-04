# postgres_docker_starter

[Learn how to use postgres sql with docker](https://www.youtube.com/watch?v=A8dErdDMqb0)

## Agenda

### 1. Create a Postgres docker container
```bash
docker run --name demo -e POSTGRES_PASSWORD=password -d postgres
```

### 2. Connect and run some queries
```bash
docker exec -it demo psql -U postgres
```
### 3. Automate - run scripts using docker CLI

## Connecting using GUI
- download dbeaver
