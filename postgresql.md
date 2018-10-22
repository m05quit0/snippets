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

#### Накатить базу из дампа.
```sh
psql -h host -U user -W -d dbname -1 -f dump.sql
```
