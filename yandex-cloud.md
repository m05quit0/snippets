[В начало](README.md)

# Yandex Cloud

#### Загрузить файлы из локальной папки в бакет Object Storage
```cmd
aws --endpoint-url=https://storage.yandexcloud.net s3 cp --recursive D:/local/dir/ s3://backet_name/remote/dir/
```