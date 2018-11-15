# 03x03 - Trabalhando na Linha de Comando - Comandos Sequenciais, history, man (103.1)

## Execução de comandos sequencial

### ;

```
$ date
Qui Nov 15 15:32:16 -03 2018
$ pwd
/home/xubuntu
$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
```

```
$ pwd; date; ls
/home/xubuntu
Qui Nov 15 15:33:02 -03 2018
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
```

### &&

Executa comandos na sequencia se o comando anterior for executado com sucesso.

```
$ ls /tmp/teste && echo Linux
ls: cannot access '/tmp/teste': No such file or directory
```

```
$ ls /tmp/ && echo Linux
16.html  39.html            firefox_xubuntu                                                               Temp-8f5e77a4-ba44-4f38-afec-7b25498c342a
23.html  config-err-eyYP6R  systemd-private-7c1c3759a9a746b7bbd997f6ac145af3-rtkit-daemon.service-FPeZj4  tmpaddon
Linux
xubuntu@xubuntu-vm:~$ 
```

### ||

Excuta comandos na sequencia, aprando a execução quando o resultado da execução for um sucesso.

```
$ date || echo Linux
Qui Nov 15 15:36:18 -03 2018

$ ls /tmp/test || echo Linux || date
ls: cannot access '/tmp/test': No such file or directory
Linux
```

## Historico


### history

[Man Page](http://man7.org/linux/man-pages/man3/history.3.html)

```
$ history 
    1  history
    2  pwd
    3  echo Linux
    4  date
    5  ls
    6  history 
```

### !!

Executa ultimo comando executado

```
$ date
Qui Nov 15 15:39:18 -03 2018
xubuntu@xubuntu-vm:~$ !!
date
Qui Nov 15 15:39:21 -03 2018
```

### ! + numero do comando do arquivo history

```
$ !3
echo Linux
Linux
```

### ! + string

```
$ !dat
date
Qui Nov 15 15:40:46 -03 2018
```

### Ctrl + R

Pesquisa de comandos digitados

```
(reverse-i-search)`': 
```

### [TAB]

Auto completa comandos

```
$ ls<TAB>
ls           lsblk        lscpu        lshw         lsipc        lslogins     lsof         lspcmcia     lsusb        
lsattr       lsb_release  lsdiff       lsinitramfs  lslocks      lsmod        lspci        lspgpot      

$ lsi<TAB>
lsinitramfs  lsipc   
```

## Buscando informações

### Man

[Man Page](http://man7.org/linux/man-pages/man1/man.1.html)

```
$ man [command name]
```

```
$ man -k "system information"
dumpe2fs (8)         - dump ext2/ext3/ext4 filesystem information
inxi (1)             - Command line system information script for console and IRC
uname (1)            - print system information
```

### info

[Man Page](https://linux.die.net/man/1/info)

Arquivo de informação mais simples.

```
$ info [command name]
```

### whatis

[Man Page](http://man7.org/linux/man-pages/man1/whatis.1.html)

```
$ whatis fwupdate
fwupdate (1)         - update system firmware
$ whatis tar
tar (1)              - The GNU version of the tar archiving utility
```

### apropos

[Man Page](http://man7.org/linux/man-pages/man1/apropos.1.html)

```
$ apropos "update system"
fwupdate (1)         - update system firmware
```