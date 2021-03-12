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

#### Исправить примечание к последнему коммиту
```sh
git commit --amend -m "New commit message"
```

#### Создать коммит, отменяющий последние 4 коммита
```sh
git revert HEAD~3..
```

#### Отменить последние 4 коммита без следов в истории
```sh
git revert --no-commit HEAD~3..
```
или
```sh
git reset --hard HEAD~3
```
