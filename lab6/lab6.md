## 3 часть, уровень Expert

### Создайте в своей домашней директорию файл под названием shared.txt. Объясните, какими правами доступа он обладает (для этого можно воспользоваться командой ls -la)


```console
kabanpunk@kabanpunk-vm:~$ touch shared.txt
kabanpunk@kabanpunk-vm:~$ ls -la
итого 748
drwxr-xr-x 16 kabanpunk kabanpunk   4096 дек  9 00:19  .
drwxr-xr-x  3 root      root        4096 ноя  1 22:39  ..
-rwxr-xr-x  1 kabanpunk kabanpunk  16696 дек  8 23:51  a.out
-rw-------  1 kabanpunk kabanpunk   2241 ноя 18 15:19  .bash_history
-rw-r--r--  1 kabanpunk kabanpunk    220 ноя  1 22:39  .bash_logout
-rw-r--r--  1 kabanpunk kabanpunk   3771 ноя  1 22:39  .bashrc
drwx------ 16 kabanpunk kabanpunk   4096 ноя  2 15:28  .cache
drwxr-x--- 14 kabanpunk kabanpunk   4096 ноя  3 20:39  .config
-rw-r--r--  1 kabanpunk kabanpunk 653185 ноя 18 15:34  crusoe.txt
drwx------  3 kabanpunk kabanpunk   4096 ноя  2 15:30  .gnupg
-rw-r--r--  1 kabanpunk kabanpunk     25 ноя 18 15:35  in
drwx------  3 kabanpunk kabanpunk   4096 ноя  1 23:49  .local
-rw-r--r--  1 kabanpunk kabanpunk     69 дек  8 23:51  main.c
drwx------  5 kabanpunk kabanpunk   4096 ноя  2 09:59  .mozilla
-rw-r--r--  1 kabanpunk kabanpunk    807 ноя  1 22:39  .profile
-rw-r--r--  1 kabanpunk kabanpunk      0 дек  9 00:19  shared.txt
drwx------  2 kabanpunk kabanpunk   4096 ноя  2 15:30  .ssh
-rw-r--r--  1 kabanpunk kabanpunk      0 дек  8 23:39  .tmp
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49  Видео
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49  Документы
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  2 15:50  Загрузки
drwxr-xr-x  3 kabanpunk kabanpunk   4096 ноя  2 15:48  Изображения
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49  Музыка
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49  Общедоступные
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49 'Рабочий стол'
drwxr-xr-x  2 kabanpunk kabanpunk   4096 ноя  1 23:49  Шаблоны
```

### C помощью команды chmod сделайте так, чтобы созданный файл был доступен только его владельцу и только на чтение. 

```console
kabanpunk@kabanpunk-vm:~$ chmod u+r shared.txt
kabanpunk@kabanpunk-vm:~$ chmod o-rwx shared.txt
```

### С помощью команды chown сделайте вашего соседа справа владельцем файла shared.txt

```console
kabanpunk@kabanpunk-vm:~$ chown right-hand-man ./shared.txt 
