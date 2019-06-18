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

#### Установить Python3.7 из исходников на Debian/Ubuntu
```sh
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
cd /usr/src
sudo wget https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tgz
sudo tar xzf Python-3.7.3.tgz
cd Python-3.7.3
sudo ./configure --enable-optimizations
sudo make altinstall
python3.7 -V
```
