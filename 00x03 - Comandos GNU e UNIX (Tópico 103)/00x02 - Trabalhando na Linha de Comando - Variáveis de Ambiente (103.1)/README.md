# 00x02 - Trabalhando na Linha de Comando - Variáveis de Ambiente (103.1)

### Declaração

```
$ NOME_VARIAVEL=valor
$ echo $NOME_VARIAVEL
valor
```

### export

[Man Page](http://man7.org/linux/man-pages/man1/export.1p.html)

```
$ TESTE=Linux

$ ./Script_Variavel.sh 
O Script lê e imprime o valor da variavel TESTE
 
O valor da variavel TESTE é:

$ export TESTE

$ ./Script_Variavel.sh 
O Script lê e imprime o valor da variavel TESTE
 
O valor da variavel TESTE é:  Linux
```

```
$ NOME_VARIAVEL=valor
$ echo $NOME_VARIAVEL
valor
$ bash
$ echo $NOME_VARIAVEL

$ exit
exit
$ export NOME_VARIAVEL
$ bash
$ echo $NOME_VARIAVEL
valor
```

### Listagem de variaveis

#### set

[Man Page](http://man7.org/linux/man-pages/man1/set.1p.html)

```
$ set | less
```

#### env

Variaveis Globais (export)

[Man Page](http://man7.org/linux/man-pages/man1/env.1.html)

```
$ env | less
```

Modificando o valor da variavel apenas na execução do comando (env):

```
$ env TESTE=Windows ./Script_Variavel.sh 
O Script lê e imprime o valor da variavel TESTE
 
O valor da variavel TESTE é:  Windows

$ echo $TESTE
LINUX
```

### unset

[Man Page](http://man7.org/linux/man-pages/man1/unset.1p.html)

```
$ unset TESTE
$ echo $TESTE

```

### Variaveis importantes

* HISTFILE	: arquivo de historico de comandos
* HOME 		: Local da **home** do usuario logado
* LOGNAME	: nome do usuario logado
* PATH		: 
* PWD		: armazena o local diretorio atual
* SHELL 	: imprime dados do shell utilizado
* TERM 		:
* USER 		:

* **$$**: Exibe número do PID do processo atual

```
$ echo $$
11184
```

* **$!**: Exibe número do PID do ultimo processo executado em background

```
$ top &

$ echo $!
12151
```

* **$?**: Exibe valor de retorno do ultimo processo executado
	* 0: Sucesso

```
$ ls /
bin  boot  cdrom  dev  etc  home  initrd.img  initrd.img.old  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var  vmlinuz  vmlinuz.old

$ echo $?
0
```

* **~**: Exibe home do usuario

```
$ echo ~
/home/xubuntu

$ echo ~root
/root
```