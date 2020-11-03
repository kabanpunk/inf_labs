# Курс информатики, семинар #1

## 1 часть, уровень Novice
### Создайте директорию, создайте файл, поперемещайте и покопируйте их. Попытайтесь удалить созданную директорию.

```console
kabanpunk@kabanpunk-vm:~$ mkdir temp
kabanpunk@kabanpunk-vm:~$ cd temp
kabanpunk@kabanpunk-vm:~/temp$ touch tmpfile
kabanpunk@kabanpunk-vm:~/temp$ ls
tmpfile
kabanpunk@kabanpunk-vm:~/temp$ mkdir dir4mv
kabanpunk@kabanpunk-vm:~/temp$ mkdir dir4cp
kabanpunk@kabanpunk-vm:~/temp$ ls
dir4cp  dir4mv  tmpfile
kabanpunk@kabanpunk-vm:~/temp$ mv tmpfile ./dir4mv
kabanpunk@kabanpunk-vm:~/temp$ cd ./dir4mv
kabanpunk@kabanpunk-vm:~/temp/dir4mv$ ls
tmpfile
kabanpunk@kabanpunk-vm:~/temp/dir4mv$ cp tmpfile /home/kabanpunk/temp/dir4cp
kabanpunk@kabanpunk-vm:~/temp/dir4mv$ cd /home/kabanpunk/temp/dir4cp
kabanpunk@kabanpunk-vm:~/temp/dir4cp$ ls
tmpfile
kabanpunk@kabanpunk-vm:~/temp/dir4cp$ pwd
/home/kabanpunk/temp/dir4cp
kabanpunk@kabanpunk-vm:~/temp/dir4cp$ cd
kabanpunk@kabanpunk-vm:~$ rm -r /home/kabanpunk/temp
kabanpunk@kabanpunk-vm:~$ ls
 Видео       Загрузки      Музыка         'Рабочий стол'
 Документы   Изображения   Общедоступные   Шаблоны
```
### Каков полный путь до вашей домашней директории? 
```console
/home/kabanpunk/
```
### Что делает команда cd без параметров? 
Перемещает в домашнюю директорию.
### Чем отличается cat от less?
Основное отличие в том, что less позволяет читать файл постранично.

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

## 3 часть, уровень Expert

### Найти количество упоминаний слова “Friday” в большом текстовом файле. 
```console
kabanpunk@kabanpunk-vm:~$ grep -o 'Friday' crusoe.txt | wc -l
188
```

### Заменить в текстовом файле все слова “Friday” на “Saturday”
```console
kabanpunk@kabanpunk-vm:~$ sed 's/Friday/Saturday/' crusoe.txt
```

### Подсчитать сумму чисел по столбцам 
```console
kabanpunk@kabanpunk-vm:~$ touch in
kabanpunk@kabanpunk-vm:~$ nano in
kabanpunk@kabanpunk-vm:~$ cat in
1 2
2 2
3 7
kabanpunk@kabanpunk-vm:~$ cat in | awk '{sl+=$1; sr+=$2} END {printf sl " " sr "\n"}'
6 11
```
