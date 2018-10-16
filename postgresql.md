[В начало](README.md)

# PostgreSQL

#### Удалить базу данных и пользователя.
```sh
sudo su postgres
dropdb dbname
dropuser username
```

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

#### Выдать пользователю права суперпользователя
```sql
ALTER USER myuser WITH SUPERUSER;
```
