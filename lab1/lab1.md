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
