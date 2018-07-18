# bandit9 -> 10

Senha no arquivo data.txt em uma das poucas strings human-readable e que começa com vários "=".

> A flag -a força um arquivo binário a ser tratado como texto.

```
$ cat data.txt | grep -a =
...
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
...
```

##### Chave:
> _truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk_