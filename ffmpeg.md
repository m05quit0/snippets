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

#### Порезать видео на куски по 1 минуте
```sh
ffmpeg -i input.mp4 -c copy -map 0 -segment_time 00:01:00 -f segment -reset_timestamps 1 output%03d.mp4
```

#### Конвертировать сферическое видео в обычную перспективу
```sh
ffmpeg -i input.mp4 -vf "v360=e:flat:h_fov=120:v_fov=90:yaw=180, scale=1920:-1" output.mp4
```