## bandit18 -> 19

A chave está num arquivo readme na pasta home, mas o .bashrc foi configurado para deslogar assim que logarmos, então tentaremos pegar o arquivo evitando carregar o .bashrc.


```
$ ssh -t bandit18@bandit.labs.overthewire /bin/sh
$ ls
readme
$ cat readme
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

##### Chave:
> _IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x_