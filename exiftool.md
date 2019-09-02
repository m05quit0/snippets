[В начало](README.md)

# exiftool

#### Извлечь гео-данные из медиа-файла
```sh
exiftool -ee -p gpx.fmt Vid_052.insv > Vid052.gpx
```

#### Извлечь embeded информацию из файла
```sh
exiftool -ee -G3 FILE
```