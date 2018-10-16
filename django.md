[В начало](README.md)

# Django

### Установка дополнительных пакетов Ubuntu для разработки на Django

#### Python
```sh
sudo apt-get install python-dev python-pip
sudo -H pip install -U pip
sudo -H pip install -U virtualenv
```

#### MySQL
```sh
sudo apt-get install mysql-server python-mysqldb libmysqlclient-dev
```

#### PostgreSQL
```sh
sudo apt-get install libpq-dev postgresql postgresql-server-dev-all postgresql-contrib
```

#### GIS
```sh
sudo apt-get install binutils libproj-dev gdal-bin
```

#### PostGIS
```sh
sudo apt-get install postgresql-x.x-postgis-x.x postgresql-x.x-postgis-scripts
```

#### Pillow (PIL)
```sh
sudo apt-get install libjpeg-dev libpng-dev libwebp-dev libtiff-dev zlib1g-dev python-imaging
```

#### lxml
```sh
sudo apt-get install python-lxml libxml2 libxml2-dev libxslt-dev
```

#### Memcached
```sh
sudo apt-get install memcached libmemcached-dev
```

#### Redis
```sh
sudo apt-get install redis-server python-redis
```

#### bcrypt
```sh
sudo apt-get install bcrypt libffi-dev
```
