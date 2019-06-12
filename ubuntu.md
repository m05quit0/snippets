[В начало](README.md)

# Ubuntu

#### Добавить локаль
Проверить список уже поддерживаемых локалей.
```sh
locale -a
```
Добавить недостающие локали.
```sh
sudo locale-gen ru_RU
sudo locale-gen ru_RU.UTF-8
```
Обновить.
```sh
sudo update-locale
```

#### Удалить пользователя из группы
```sh
sudo deluser username groupname
```

#### Создать swap для тяжелых задач на слабом сервере
```sh
sudo dd if=/dev/zero of=/swapfile bs=1024 count=524288
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```
Чтобы своп подключался автоматически при загрузке, добавить в /etc/fstab:
```
/swapfile   swap    swap    defaults        0       0
```
