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
