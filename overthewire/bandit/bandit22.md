## bandit21 -> 22

A chave está relacionada a programas do cron.

```
$ ls /etc/cron.d
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  popularity-contest
$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

Então sabemos que a chave está no arquivo _/tmp/t7t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv_
```
$ cat /tmp/Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

##### Chave:
> _Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI_