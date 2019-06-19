[В начало](README.md)

# Python

#### Удалить все пакеты в виртуальном окружении

```sh
pip uninstall -y -r <(pip freeze)
```

#### Сгенерировать случайную строку
```sh
python -c "import os; print(os.urandom(16))"
```

#### В Windows установить mysqlclient и некоторые другие бинарные пакеты в прекомпилированном виде, чтобы не возиться с установкой Visual Studio Build Tools.

Скачать пакет с https://www.lfd.uci.edu/~gohlke/pythonlibs/

```sh
pip install <имя-пакета>.whl
```

#### HTTP сервер для раздачи статики из директории (Python 3).
```sh
python -m http.server
```

#### Установить Python 3.7 из исходников на Debian/Ubuntu
```sh
sudo apt install -y build-essential checkinstall
sudo apt install -y wget build-essential libffi-dev libgdbm-dev libc6-dev libssl-dev zlib1g-dev libbz2-dev libreadline-dev  libsqlite3-dev libncurses5-dev libncursesw5-dev xz-utils tk-dev
cd /usr/src
sudo wget https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tgz
sudo tar xzf Python-3.7.3.tgz
cd Python-3.7.3
sudo ./configure --enable-optimizations
sudo make altinstall
python3.7 -V
```
