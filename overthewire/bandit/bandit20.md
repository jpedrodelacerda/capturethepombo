## bandit19 -> 20

Para alcançar o próximo nível devemos utilizar o binário setuid na pasta home.

```
$ ./bandit20-do 
Run a command as another user.
  Example: ./bandit20-do id
```

Então basta lermos o arquivo /etc/bandit_pass/bandit20 como o usuário bandit20.

```
./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

##### Chave:
> _GbKksEFF4yrVs6il55v6gwY5aVje5f0j_