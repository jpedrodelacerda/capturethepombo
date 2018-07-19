## bandit20 -> 21

O binário _suconnect_ cria uma conexão com o localhost na porta TCP especificada e lê uma linha para compará-la com a chave do bandit20. Se for correta, retorna a chave do bandit21.

```
$ ./suconnect 
Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
```

Então utilizaremos o tmux:

Para iniciar o tmux: ```$ tmux```

Para criar um novo painel:```C-b %```

Para alternar entre os painéis:```C-b <seta>```

Então com os dois painéis, basta iniciarmos o daemon em alguma porta e no outro painel enviar a chave utilizando o netcat.
> Utilizar _nc -l_ para que o daemon _suconnect_ consiga iniciar a conexão na porta.

Terminal A
```
$ nc -l 127.0.0.1 <porta>
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```

Terminal B
```
$ ./suconnect <porta>
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
```

##### Chave:
> _gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr_