# Trabalhando na Linha de Comando - uname, alias (103.1)

## uname

[Man Page](http://man7.org/linux/man-pages/man1/uname.1.html)

```
$ uname
Linux
$ uname -a
Linux xubuntu-vm 4.15.0-39-generic #42~16.04.1-Ubuntu SMP Wed Oct 24 17:09:54 UTC 2018 x86_64 x86_64 x86_64 GNU/Linux
```

## alias

```
$ alias
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias grep='grep --color=auto'
alias l='ls -CF'
alias la='ls -A'
alias ll='ls -alF'
alias ls='ls --color=auto'
```

```
$ alias lt='ls /tmp'
$ lt
16.html
23.html
39.html
57.html
config-err-eyYP6R
systemd-private-7c1c3759a9a746b7bbd997f6ac145af3-rtkit-daemon.service-FPeZj4
Temp-8f5e77a4-ba44-4f38-afec-7b25498c342a
tmpaddon
```