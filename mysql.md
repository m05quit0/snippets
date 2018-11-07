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

#### Открыть доступ к БД внешнему пользователю.
Открыть файл конфига.
```sh
sudo vi /etc/mysql/mysql.conf.d/mysql.cnf
```
Изменить опцию `bind-address` c `127.0.0.1` на `0.0.0.0`.
Перезагрузить сервер.
```sh
sudo service mysql restart
```
Разрешить пользователю доступ с любого хоста или создать нового пользователя.
```sql
UPDATE `mysql`.`user` SET `Host` = '%' WHERE `User`='username' limit 1;
FLUSH PRIVILEGES;
```
Разрешить пользователю доступ к нужной БД.
```sql
GRANT ALL PRIVILEGES ON `dbname`.* TO `username`@'%';
FLUSH PRIVILEGES;
```
