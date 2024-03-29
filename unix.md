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
cd my_dir/ && tar -zcf ../my_dir.tgz . && cd ..
```

#### Распаковать tar.gz в нужную директорию
```sh
mkdir foo
tar -xzf bar.tar.gz -C foo
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

#### Закнуть свой публичный ключ на сервер в ~/.ssh/authorized_keys
```sh
ssh-copy-id username@hostname
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

#### Распечатать все текстовые исходники приложения в один файл. Например, для депонирования авторских прав.
```sh
for i in `find package.json README.md public src -type f \( ! -iname "*.jpg" -and ! -iname "*.png" \)`; do echo "$i"; echo "---"; cat "$i"; echo ; done > all_source.txt
```

#### Переименовать файлы в папке с числами в имени с заполнением нулями по маске.
```sh
rename 's/\d+/sprintf("%05d",$&)/e' *.jpg
```

## Ссылки
- [Изучите необходимый минимум Linux, чтобы быть продуктивным](https://ru.hexlet.io/blog/posts/basic-linux-productivity)
