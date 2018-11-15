# 00x03 - Comandos GNU e UNIX (Tópico 103)

## Trabalhando na Linha de Comando - shell, bash, echo, type, PATH ()

Nessa aula serão abordados os seguintes assuntos:
* shell
* bash
* comando echo
* comando type
* PATH

---

### echo

[Man page](http://man7.org/linux/man-pages/man1/echo.1.html)

```
$ echo "Hello World!"
Hello World!

$ echo "Linux Ubuntu"
Linux Ubuntu
```

### variaveis

```
$ echo $SHELL
/bin/bash
```

### type

[Man Page](http://man7.org/linux/man-pages/man1/type.1p.html)

```
$ type echo
echo is a shell builtin

$ type cd
cd is a shell builtin
```

```
$ type clear
clear is hashed (/usr/bin/clear)
```

```
$ type tar
tar is /bin/tar
```

### $PATH

```
$ echo $PATH
/home/xubuntu/bin:/home/xubuntu/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/biǹ
```

### pwd

```
$ pwd
/home/xubuntu
```

### cd

[Man Page](http://man7.org/linux/man-pages/man1/cd.1p.html)

```
$ cd /
```

### ls

[Man Page](http://man7.org/linux/man-pages/man1/pwd.1.html)

```
$ ls
bin  boot  cdrom  dev  etc  home  initrd.img  initrd.img.old  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var  vmlinuz  vmlinuz.old
```

### Executando scripts

```
$ ./Script_Exemplo.sh
Script Run...
Qui Nov 15 14:56:37 -03 2018
Bye!
```

```
$ ./Documents/projects/Linux-LPIC1/00x03\ -\ Comandos\ GNU\ e\ UNIX\ \(Tópico\ 103\)/files/Script_Exemplo.sh 
Script Run...
Qui Nov 15 14:57:31 -03 2018
Bye!
```