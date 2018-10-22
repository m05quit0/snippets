[В начало](README.md)

#### Загрузить таблицы временных зон.
```sh
mysql_tzinfo_to_sql /usr/share/zoneinfo | mysql -u root mysql
```
[Подробнее о временных зонах в MySQL](https://dev.mysql.com/doc/refman/8.0/en/time-zone-support.html)
