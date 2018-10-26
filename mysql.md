[В начало](README.md)

#### Создать базу данных и пользователя
```sh
mysql -u root -p
```
```sql
CREATE DATABASE `dbname`;
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON `dbname`.* TO 'username'@'localhost';
FLUSH PRIVILEGES;
```

#### Назначить пользователю права суперпользователя
```sql
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

#### Создать дамп базы
```sh
mysqldump -h host -u user -p dbname > dump.sql
```

#### Накатить базу из дампа
```sh
mysql -h host -u user -p dbname < dump.sql
```

#### Загрузить таблицы временных зон.
```sh
mysql_tzinfo_to_sql /usr/share/zoneinfo | mysql -u root mysql
```
[Подробнее о временных зонах в MySQL](https://dev.mysql.com/doc/refman/8.0/en/time-zone-support.html)
