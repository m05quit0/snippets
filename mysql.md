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

#### Загрузить таблицы временных зон.
```sh
mysql_tzinfo_to_sql /usr/share/zoneinfo | mysql -u root mysql
```
[Подробнее о временных зонах в MySQL](https://dev.mysql.com/doc/refman/8.0/en/time-zone-support.html)