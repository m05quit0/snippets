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
