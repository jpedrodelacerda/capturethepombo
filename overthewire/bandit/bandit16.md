## bandit15 -> 16

A chave para o próximo nível é obtida depois de submeter a chave do nível 15 na porta 30001 do local host com SSL.

```
$ openssl s_client -ign_eof -connect 127.0.0.1:30001
---
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd

closed
```

##### Chave:
> _cluFn7wTiGryunymYOu4RcffSxQluehd_