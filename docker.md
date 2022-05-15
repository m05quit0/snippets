[В начало](README.md)

# Docker

#### Залить дамп базы данных PostgreSQL
```sh
docker exec -i container_id psql -h localhost -U db_user -W -d db_name -1 < dump.sql
```