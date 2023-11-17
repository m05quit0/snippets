[В начало](README.md)

# Docker Compose

#### Удалить volume
```sh
# Stop and remove container's using the target volume
docker-compose stop NAME_OF_CONTAINER

# We need the force flag, "-f", as the container is still bound to the volume
docker-compose rm -f NAME_OF_CONTAINER

# Next find your volume name in the following list
docker volume ls

# Finally remove the volume
docker volume rm VOLUME_NAME
```

#### Сделать дамп PostgreSQL
```sh
docker-compose exec postgres pg_dump -c -U dbuser dbname --no-owner > db-dump.sql
```

#### Сделать gzip дамп PostgreSQL
```sh
docker-compose exec postgres pg_dump -c -U dbuser dbname --no-owner | gzip -9 > db-dump.sql.gz
```

#### Накатить дамп PostgreSQL
```sh
cat db-dump.sql | docker-compose exec -T postgres psql -U dbuser dbname
```

#### Накатить gzip дамп PostgreSQL
```sh
gunzip -c db-dump.sql.gz | docker-compose exec -T postgres psql -U dbuser dbname
```
