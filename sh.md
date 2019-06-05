[В начало](README.md)

# Unix shell

#### Отсортировать и оставить только уникальные строки в файле
```sh
sort file.txt | uniq >> temp && mv temp file.txt
```

#### Проверить, не битая ли картинка
```sh
convert path_to_image null: 2>&- || echo File is corrupted
```

#### Создать архив директории
```sh
cd my_dir/ && tar -zcvf ../my_dir.tgz . && cd ..
```

#### Вывести листинг директории с указанием размера файлов в MiB
```
ls -l --block-size=M
```

#### Проверить работоспособность SMTP сервера
```sh
sudo apt install swaks
swaks -t user@example.com -s smtp.gmail.com:587 -tls -a LOGIN
```

#### Сгенерировать пару SSH ключей
```sh
ssh-keygen
```

## Ссылки
- [Изучите необходимый минимум Linux, чтобы быть продуктивным](https://ru.hexlet.io/blog/posts/basic-linux-productivity)
