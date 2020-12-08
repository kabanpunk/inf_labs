## 2 часть, уровень Advanced

### С помощью команд which и whereis выясните, в какой директории находятся программы cat, less, grep и find

```console
kabanpunk@kabanpunk-vm:~$ which cat
/usr/bin/cat
kabanpunk@kabanpunk-vm:~$ whereis cat
cat: /usr/bin/cat /usr/share/man/man1/cat.1.gz
```

### Выведите на экран значение переменной окружения $PATH (echo $PATH) и убедитесь, что директория, найденная в п.1 входит в $PATH

```console
kabanpunk@kabanpunk-vm:~$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```

### Скомпилируйте какую-нибудь программу на C и попробуйте запустить её, находясь в той же директории. Перейдите в другую директорию и запустите ту же программу.


```console
kabanpunk@kabanpunk-vm:~$ nano
kabanpunk@kabanpunk-vm:~$ cat main.c
#include <stdio.h>
 
int main() {
	printf("hi, dude\n");
	return 0;
}
kabanpunk@kabanpunk-vm:~$ gcc main.c
kabanpunk@kabanpunk-vm:~$ ls
 a.out        in       Видео       Загрузки      Музыка         'Рабочий стол'
 crusoe.txt   main.c   Документы   Изображения   Общедоступные   Шаблоны  
kabanpunk@kabanpunk-vm:~$ ./a.out
hi, dude
kabanpunk@kabanpunk-vm:~$ cd 'Загрузки/' 
kabanpunk@kabanpunk-vm:~/Загрузки$ /home/kabanpunk/a.out
hi, dude
```

### Добавьте директорию, в которой лежит программа из п.3 в $PATH (export PATH=$PATH:<новая директория>). 


```console
kabanpunk@kabanpunk-vm:~/Загрузки$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
kabanpunk@kabanpunk-vm:~/Загрузки$ export PATH=$PATH:/home/kabanpunk
kabanpunk@kabanpunk-vm:~/Загрузки$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/kabanpunk
```

