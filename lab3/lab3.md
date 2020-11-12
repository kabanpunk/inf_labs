## 3 часть, уровень Expert

### Найти количество упоминаний слова “Friday” в большом текстовом файле. 
```console
kabanpunk@kabanpunk-vm:~$ grep -o 'Friday' crusoe.txt | wc -l
188
```

### Заменить в текстовом файле все слова “Friday” на “Saturday”
```console
kabanpunk@kabanpunk-vm:~$ sed 's/Friday/Saturday/g' crusoe.txt
```

### Вывести строку, содержащую больше всего чисел
```console
kabanpunk@kabanpunk-vm:~$ touch in
kabanpunk@kabanpunk-vm:~$ nano in
kabanpunk@kabanpunk-vm:~$ cat in
1 300
2 3
10
kabanpunk@kabanpunk-vm:~$ cat in | awk 'BEGIN { m = -1; s = ""; } { if (NF > m) { m = NF; s = $0; } } END { print s "\n"; } '
1 300
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
