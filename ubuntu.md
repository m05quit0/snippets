# Ubuntu

#### Добавить локаль
Проверить список уже поддерживаемых локалей.
```sh
locale -a
```
Добавить недостающие локали.
```sh
sudo locale-gen ru_RU
sudo locale-gen ru_RU.UTF-8
```
Обновить.
```sh
sudo update-locale
```
