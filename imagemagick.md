[В начало](README.md)

# ImageMagick

### Сделать ресайз всех изображений в директории и переименовать по маске
```sh
for file in *.jpg; do convert $file -scale 25% -set filename:f %t_lr %[filename:f].jpg; done
```