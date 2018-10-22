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
