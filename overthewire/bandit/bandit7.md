## bandit6 -> 7

Senha em algum arquivo no servidor com as seguintes:
* owned by user
* owned by group
* 33 bytes in size

Usar o find com flags para filtrar os arquivos: 
> Lembrar de filtrar os erros com "2>/dev/null"

```
$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password

$cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

##### Chave:
> _HKBPTKQnIay4Fw76bEy8PVxKEDQRKTz_