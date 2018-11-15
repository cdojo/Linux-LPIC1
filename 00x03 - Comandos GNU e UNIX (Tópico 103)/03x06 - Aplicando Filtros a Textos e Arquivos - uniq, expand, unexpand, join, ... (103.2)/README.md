# 03x06 - Aplicando Filtros a Textos e Arquivos - uniq, expand, unexpand, join, ... (103.2)

## uniq

[Man Page](http://man7.org/linux/man-pages/man1/uniq.1.html)

```
# uniq alunos.txt

Andre
Paulo
Carlos
Ana

Rafael
Silvia
Paulo
```

* **-d**: Exibe o conteudo duplicado no arquivo

```
# uniq -d alunos.txt

Ana
Paulo
```

* **-c**: Exibe a quatidade de conteudo duplicado no arquivo

```
# uniq -d alunos.txt

2 Ana
2 Paulo
3 Ricardo
```

## sort

[Man Page](http://man7.org/linux/man-pages/man1/sort.1.html)

```
# sort alunos.txt



Ana
Andre
Carlos
Paulo
Paulo
Rafael
Silvia
```

```
# sort alunos.txt | uniq



Ana
Andre
Carlos
Paulo
Rafael
Silvia
```

## expand

[Man Page](http://man7.org/linux/man-pages/man1/expand.1.html)

Tab para espaços

```
# expand alunos.txt
```

## unexpand

[Man Page](http://man7.org/linux/man-pages/man1/unexpand.1.html)

Espaços para Tab

* **-a**: Olhe para todos os espaços (default apenas no começo das linhas)

```
# unexpand -a alunos.txt
```

## od

[Man Page](http://man7.org/linux/man-pages/man1/od.1.html)

```
# od alunos.txt
```


## join

[Man Page](http://man7.org/linux/man-pages/man1/join.1.html)

Combina dois arquivos atraves de um indice.

```
$ cat codigo-aluno.txt 
1 Ana
2 Joao
3 Andre
4 Maria
5 Carlos

$ cat notas-alunos.txt 
1 10
2 8
3 9
4 2
5 0

$ join codigo-aluno.txt notas-alunos.txt 
1 Ana 10
2 Joao 8
3 Andre 9
4 Maria 2
5 Carlos 0
```

## paste

[Man Page](http://man7.org/linux/man-pages/man1/paste.1.html)

Combina linha a linha

```
$ paste codigo-aluno.txt notas-alunos.txt 
1 Ana	 1 10
2 Joao	 2 8
3 Andre	 3 9
4 Maria	 4 2
5 Carlos 5 0
```

## split

[Man Page](http://man7.org/linux/man-pages/man1/split.1.html)

Divide um arquivo em varios outros

* **-l**: Quantidade de linhas a ser separadas.
* **-b**: Quantidade de bytes por linha.

```
$ split -l 20 arquivo-longo.txt
```