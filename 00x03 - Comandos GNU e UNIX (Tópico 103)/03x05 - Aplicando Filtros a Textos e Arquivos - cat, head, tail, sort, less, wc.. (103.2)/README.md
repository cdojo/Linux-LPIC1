# 03x05 - Aplicando Filtros a Textos e Arquivos - cat, head, tail, sort, less, wc.. (103.2)

## cat

[Man Page](http://man7.org/linux/man-pages/man1/cat.1.html)

```
$ cat alunos.txt 
Milo Coffman  
Sharon Koening  
Herma Kendricks  

Leeanne Jolliff  
Loren Boutte  

Kristan Heims  
Taryn Dacruz  

Kyra Cornejo  
```

```
$ cat -n alunos.txt 
     1	Milo Coffman  
     2	Sharon Koening  
     3	Herma Kendricks  
     4	
     5	Leeanne Jolliff  
     6	Loren Boutte  
     7	
     8	Kristan Heims  
     9	Taryn Dacruz  
    10	
    11	Kyra Cornejo  

```

```
$ cat -b alunos.txt 
     1	Milo Coffman  
     2	Sharon Koening  
     3	Herma Kendricks  


     4	Leeanne Jolliff  
     5	Loren Boutte  

     6	Kristan Heims  
     7	Taryn Dacruz  

     8	Kyra Cornejo  
```

```
$ cat -s alunos.txt 
Milo Coffman  
Sharon Koening  
Herma Kendricks  

Leeanne Jolliff  
Loren Boutte  

Kristan Heims  
Taryn Dacruz  

Kyra Cornejo  
Cassey Carnley  
```

```
$ cat -A alunos.txt 
Milo Coffman  $
Sharon Koening  $
Herma Kendricks  $
$
Leeanne Jolliff  $
Loren Boutte  $
$
Kristan Heims  $
Taryn Dacruz  $
$
Kyra Cornejo  $
```

## tac

[Man Page](http://man7.org/linux/man-pages/man1/tac.1.html)

```
$ tac alunos.txt 
Bebe Durgan  Louis Zeolla  
Cruz Chastain  

Ima Julia  
Madalene Tocci  
Norman Sifford  
Kathrine Bichrest  

Roy Rennie
```

## head

[Man Page](http://man7.org/linux/man-pages/man1/head.1.html)

```
$ head alunos.txt 
Milo Coffman  
Sharon Koening  
Herma Kendricks  

Leeanne Jolliff  
Loren Boutte  

Kristan Heims  
Taryn Dacruz  
```

```
$ head -n4 alunos.txt 
Milo Coffman  
Sharon Koening  
Herma Kendricks  

```

```
$ head -c47 alunos.txt 
Milo Coffman  
Sharon Koening  
```

## tail

[Man Page](http://man7.org/linux/man-pages/man1/tail.1.html)

```
$ tail alunos.txt 
Roy Rennie  

Kathrine Bichrest  
Norman Sifford  
Madalene Tocci  
Ima Julia  

Cruz Chastain  
Louis Zeolla  
```

```
$ tail -f alunos.txt 
Roy Rennie  

Kathrine Bichrest  
Norman Sifford  
Madalene Tocci  
Ima Julia  

Cruz Chastain  
Louis Zeolla  
Bebe Durgan  Antony Mark

```

## less

[Man Page](http://man7.org/linux/man-pages/man1/less.1.html)

```
$ less alunos.txt
```

### Buscas

```
/ <string>
```

* Ctrl + g: status do arquivo

## wc

[Man Page](http://man7.org/linux/man-pages/man1/wc.1.html)

* Linhas, palavras, caracteres

```
$ wc alunos.txt 
 64 102 831 alunos.txt
```

```
$ wc -l alunos.txt 
64 alunos.txt

$ wc -w alunos.txt 
102 alunos.txt

$ wc -c alunos.txt 
831 alunos.txt
```

```
$ wc *
  64  102  831 alunos.txt
  45  169 1709 pwd-man.txt
 109  271 2540 total
```

## nl

[Man Page](http://man7.org/linux/man-pages/man1/nl.1.html)

```
$ nl alunos.txt 
     1	Milo Coffman  
     2	Sharon Koening  
     3	Herma Kendricks  
       
     4	Leeanne Jolliff  
     5	Loren Boutte  
       
     6	Kristan Heims  
     7	Taryn Dacruz  
       
     8	Kyra Cornejo  

```

## sort

[Man Page](http://man7.org/linux/man-pages/man1/sort.1.html)

```
$ sort alunos.txt



Alecia Poch  
Bebe Durgan  Antony Mark
Cassey Carnley  
Cruz Chastain  
Dollie Ephraim  
Dorsey Cokley  
Edmundo Erion  
Elvin Start  
Eula Madore  
Evelyn Shattles  
Gigi Speer  
Herma Kendricks  
Ima Julia
```

```
$ sort -r alunos.txt 
Violet Hardesty  
Trudie Fleenor  
Tonisha Roos  
Tiffani Byam  
Taryn Dacruz  
Stefani Jim  
Sherlene Stephens  
Sharri Tagle  
Sharon Koening  
Senaida Ostrom  
```

```
$ sort -k2 alunos.txt 


Kathrine Bichrest  
Loren Boutte  
Leonarda Boyett  
Tiffani Byam  
Cassey Carnley  
Cruz Chastain  
Milo Coffman  
Dorsey Cokley  
Kyra Cornejo  
Taryn Dacruz  
Bebe Durgan  Antony Mark
Dollie Ephraim  
```