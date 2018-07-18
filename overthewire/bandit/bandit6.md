## bandit5 -> 6

Senha em algum arquivo no diretório inhere com as seguintes propriedades:
* human-readable
* 1033 bytes in size
* not executable

Usar o find com flags para filtragem do arquivo desejado:

```
$ find inhere -size 1033c
inhere/maybehere07/.file2

$ cat inhere/maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

##### Chave:
> _DXjZPULLxYr17uwoI01bNLQbtFemEgo7_