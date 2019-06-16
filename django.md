[В начало](README.md)

# Django

### Установка дополнительных пакетов Ubuntu для разработки на Django

#### Python 2
```sh
sudo apt install python-dev python-pip
sudo -H pip install -U pip
sudo -H pip install -U virtualenv
virtualenv venv
```

#### Python 3
```sh
sudo apt install python3-dev python3-venv
sudo -H python3 -m pip install --upgrade pip
python3 -m venv venv
```

#### MySQL
```sh
sudo apt install mysql-server python-mysqldb libmysqlclient-dev
```

#### PostgreSQL
```sh
sudo apt install libpq-dev postgresql postgresql-server-dev-all postgresql-contrib
```

#### GIS
```sh
sudo apt install binutils libproj-dev gdal-bin
```

#### PostGIS
```sh
sudo apt install postgresql-x.x-postgis-x.x postgresql-x.x-postgis-scripts
```

#### Pillow (PIL)
```sh
sudo apt install libjpeg-dev libpng-dev libwebp-dev libtiff-dev zlib1g-dev python-imaging
```

#### lxml
```sh
sudo apt install python-lxml libxml2 libxml2-dev libxslt-dev
```

#### Memcached
```sh
sudo apt install memcached libmemcached-dev
```

#### Redis
```sh
sudo apt install redis-server python-redis
```

#### bcrypt
```sh
sudo apt install bcrypt libffi-dev
```

#### Сгенерировать случайный ключ, как это делает Django
```python
from django.core.management.utils import get_random_secret_key
get_random_secret_key()
```

#### Стартовать проект в текущей директории
```sh
django-admin startproject projectname .
```

#### Отображение тестовых страниц 404 и 500 в дев-окружении
```python
if settings.DEBUG:
    from django.views.generic.base import TemplateView

    urlpatterns += [
        path('test404/', TemplateView.as_view(template_name='404.html')),
        path('test500/', TemplateView.as_view(template_name='500.html')),
    ]
```
