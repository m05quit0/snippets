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

#### Сгенерировать пару RSA ключей
```sh
ssh-keygen
```

#### Принудительно залогиниться по ssh с помощью пароля
```sh
ssh -o PreferredAuthentications=password example.com
```

#### Использование диска
```sh
df -h
```

#### Навигация по консольному выводу screen сессии
- Перейти в режим скроллбек - Ctrl+a [
- Vim навигация hjkl и Ctrl+b, Ctrl+f
- Выйти из скроллбека Esc

#### Вернуться к активному screen (attached) после дисконнекта
```sh
screen -D -r session_id
```

## Ссылки
- [Изучите необходимый минимум Linux, чтобы быть продуктивным](https://ru.hexlet.io/blog/posts/basic-linux-productivity)
