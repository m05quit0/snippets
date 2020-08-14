[В начало](README.md)

# ffmpeg

#### Порезать видео на картинки
```sh
ffmpeg -i video.mp4 image%d.jpg
```

#### Порезать видео на картинки с контролем качества в диапозоне 2-31, где 31 - худшее качество.
```sh
ffmpeg -i video.mp4 -qscale:v 2 image%d.jpg
```

#### Порезать видео на картинки c необходимой частотой извлечения кадров
```sh
ffmpeg -i video.mpg -vf fps=15 image%d.jpg
```