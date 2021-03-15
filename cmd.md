[В начало](README.md)

# Windows cmd

### Создать символьную ссылку на директорию
```cmd
mklink /d \MyFolder \Users\User1\Documents
```

### Создать жесткую ссылку на файл
```cmd
mklink /h \MyFile.file \User1\Documents\example.file
```

### Заархивировать директорию в zip исключая некоторые поддиректории
```cmd
7z a -tzip arch.zip source_path -xr!?git\ -xr!?vscode\ -xr!__pycache__\
```

### Заархивировать содержимое текущей директории в zip без зжатия
```cmd
7z a -tzip -mx0 ..\arch.zip .\*
```
