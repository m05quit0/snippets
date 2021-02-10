[В начало](README.md)

# Git

#### Переименовать текущую локальную ветку
```sh
git branch -m new-branch-name
```

#### Сменить удаленный репозитарий.
```sh
git remote -v
git remote set-url origin git@repo.url
git remote -v
```

#### Удалить несколько веток по маске
```sh
git branch -d `git branch --list 'xyz*'`
```

#### Сравнить файл в двух ветках
```sh
git diff mybranch..master -- file/path
```