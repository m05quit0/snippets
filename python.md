[В начало](README.md)

# Python

#### Удалить все пакеты в виртуальном окружении

```sh
pip uninstall -y -r <(pip freeze)
```

#### Сгенерировать случайную строку
```sh
python3 -c "import uuid; print(uuid.uuid4().hex)"
```
