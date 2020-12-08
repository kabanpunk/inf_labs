## 1 часть, уровень Novice

### Создайте файл, имя которого начинается с точки. Убедитесь, что его не видно с помощью обычной команды ls 
```console
kabanpunk@kabanpunk-vm:~$ touch ./.tmp
kabanpunk@kabanpunk-vm:~$ ls
 crusoe.txt   Видео       Загрузки      Музыка         'Рабочий стол'
 in           Документы   Изображения   Общедоступные   Шаблоны 
```

### Выясните, какие скрытые файлы и директории находятся в вашей домашней директории
```console
kabanpunk@kabanpunk-vm:~$ ls -a
 .               .bashrc      .gnupg     .profile   Документы     Общедоступные
 ..              .cache       in         .ssh       Загрузки     'Рабочий стол'
 .bash_history   .config      .local     .tmp       Изображения   Шаблоны
 .bash_logout    crusoe.txt   .mozilla   Видео      Музыка
```

### Ищет ли find по скрытым файлам и директориям?

Да
```console
kabanpunk@kabanpunk-vm:~$ find ~ -type f -name ".*" 
