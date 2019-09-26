[В начало](README.md)

# ffmpeg

#### Порезать видео на картинки
```sh
ffmpeg -i video.mpg image%d.jpg
```

#### Порезать видео на картинки c необходимой частотой извлечения кадров
```sh
ffmpeg -i video.mpg -vf fps=15 image%d.jpg
```