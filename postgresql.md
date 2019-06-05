[В начало](README.md)

# PostgreSQL

#### Создать пользователя и базу данных
```sh
sudo su postgres
createuser myuser
createdb mydb
psql
```
```sql
ALTER USER myuser WITH ENCRYPTED PASSWORD 'mypass';
ALTER ROLE myuser SET client_encoding TO 'utf8';
ALTER ROLE myuser SET default_transaction_isolation TO 'read committed';
ALTER ROLE myuser SET timezone TO 'UTC';
GRANT ALL ON DATABASE mydb TO myuser;
```

#### Удалить базу данных и пользователя.
```sh
sudo su postgres
dropdb dbname
dropuser username
```

#### Выдать пользователю права суперпользователя
```sql
ALTER USER myuser WITH SUPERUSER;
```

#### Создать дамп базы.
```sh
pg_dump -h host -U user -W --no-owner dbname > dump.sql
```

#### Накатить базу из дампа.
```sh
psql -h host -U user -W -d dbname -1 -f dump.sql
```

#### Сделать дамп на другой сервер без создания файла.
```sh
pg_dump dbname | psql dbname
```

#### Показать все таблицы в текущей базе
```psql
\dt
```
