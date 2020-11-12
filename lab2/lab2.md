## 2 часть, уровень Advanced
### Скачайте крупный текстовый файл 

```console
kabanpunk@kabanpunk-vm:~$ wget http://factorized.net/crusoe.txt
--2020-11-03 20:15:08--  http://factorized.net/crusoe.txt
Распознаётся factorized.net (factorized.net)… 185.199.108.153, 185.199.109.153, 185.199.110.153, ...
Подключение к factorized.net (factorized.net)|185.199.108.153|:80... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 652809 (638K) [text/plain]
Сохранение в: «crusoe.txt»
 
crusoe.txt          100%[==================>] 637,51K   119KB/s    за 5,6s    
 
2020-11-03 20:15:15 (113 KB/s) - «crusoe.txt» сохранён [652809/652809]
``` 

### Найти все файлы *.txt в папке /tmp
```console
kabanpunk@kabanpunk-vm:~$ ls
 crusoe.txt   Документы   Изображения   Общедоступные   Шаблоны
 Видео        Загрузки    Музыка       'Рабочий стол'
kabanpunk@kabanpunk-vm:~$ mkdir tmp 
kabanpunk@kabanpunk-vm:~$ mv crusoe.txt tmp  
kabanpunk@kabanpunk-vm:~$ find ./tmp -type f -name '*.txt'
./tmp/crusoe.txt 
```

### Найти все строки "friday" в большом текстовом файле
```console
kabanpunk@kabanpunk-vm:~$ cd tmp
kabanpunk@kabanpunk-vm:~/tmp$ grep -o 'friday' crusoe.txt
kabanpunk@kabanpunk-vm:~/tmp$ grep -o -i 'friday' crusoe.txt
Friday
Friday
Friday
...
Friday
```

### С помощью > и >> записать в текстовый файл фразу "Hello world"
```console
kabanpunk@kabanpunk-vm:~/tmp$ echo 'Hello world' > crusoe.txt
kabanpunk@kabanpunk-vm:~/tmp$ cat crusoe.txt 
Hello world
kabanpunk@kabanpunk-vm:~/tmp$ echo 'append another "Hello world"' >> crusoe.txt 
kabanpunk@kabanpunk-vm:~/tmp$ cat crusoe.txt 
Hello world
append another "Hello world" 
```

### Вывести в файл список файлов в текущей директории
```console
kabanpunk@kabanpunk-vm:~/tmp$ ls > crusoe.txt
kabanpunk@kabanpunk-vm:~/tmp$ cat crusoe.txt
crusoe.txt
```

### Попробовать найти все файлы *.txt на всём диске. Придумать, как уменьшить количество мусора, выводимого на экран этой командой
```console
kabanpunk@kabanpunk-vm:~$ find ./ -type f -name '*.txt'
./.mozilla/firefox/sw7qy5op.default-release/TRRBlacklist.txt
./.mozilla/firefox/sw7qy5op.default-release/SiteSecurityServiceState.txt
./.mozilla/firefox/sw7qy5op.default-release/SecurityPreloadState.txt
./.mozilla/firefox/sw7qy5op.default-release/AlternateServices.txt
./.mozilla/firefox/sw7qy5op.default-release/pkcs11.txt
./tmp/crusoe.txt
./.cache/tracker/db-version.txt
./.cache/tracker/db-locale.txt
./.cache/tracker/parser-version.txt
./.cache/tracker/first-index.txt
./.cache/tracker/last-crawl.txt  
kabanpunk@kabanpunk-vm:~$ find ./ -type f -name '*.txt' -printf '%f\n'
TRRBlacklist.txt
SiteSecurityServiceState.txt
SecurityPreloadState.txt
AlternateServices.txt
pkcs11.txt
crusoe.txt
db-version.txt
db-locale.txt
parser-version.txt
first-index.txt
last-crawl.txt
```
