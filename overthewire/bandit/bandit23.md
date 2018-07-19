## bandit22 -> 23

A chave está, novamente, ligada à um script ligado pelo cron.

```
$ ls /etc/cron.d/
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  popularity-contest
$ cat /etc/cron.d/cronjob_bandit23 
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
$ cat /usr/bin/cronjob_bandit23.sh 
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```
Para descobrirmos o valor de _$mytarget_ basta rodarmos o comando substituindo o $myname por bandit23, que é quem executa o script.
```
$ echo $(echo I am user bandit23| md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
```

Logo, a chave está no arquivo /tmp/8ca319486bfbbc3663ea0fbe81326349
```
$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

##### Chave:
> _jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n_