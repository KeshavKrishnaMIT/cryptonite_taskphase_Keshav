# Killing Processes
This challenge is a bit problematic, I tried certain things initially and they didnt work, and I dont know why my terminal stopped working. I'll show it----
```bash
Connected!
hacker@processes~killing-processes:~$ /challenge/run
Nope! /challenge/dont_run is still running! You gotta terminate it before I
give you the flag!
hacker@processes~killing-processes:~$ ps -e | /challenge/run
Nope! /challenge/dont_run is still running! You gotta terminate it before I
give you the flag!
hacker@processes~killing-processes:~$ kill /challenge/dont_run
ssh-entrypoint: kill: /challenge/dont_run: arguments must be process or job IDs
hacker@processes~killing-processes:~$ ps -e | grep /challenge/dont_run
hacker@processes~killing-processes:~$ ps aux | grep /challenge/dont_run
hacker        73  0.0  0.0   4976  3520 ?        Ss   13:53   0:00 /challenge/dont_run
hacker       104  0.0  0.0   4140  2240 pts/0    S+   13:57   0:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ ps -ef | /challenge/dont_run
```
Probably because I forgot to write grep in my last command,
```bash
root@ZEROBOOK13:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@processes~killing-processes:~$ ps -e | grep /challenge/dont_run
hacker@processes~killing-processes:~$ ps -ef | grep /challenge/dont_run
hacker        74      72  0 14:01 ?        00:00:00 /challenge/dont_run
hacker        96      76  0 14:01 pts/0    00:00:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 74
hacker@processes~killing-processes:~$ kill 72
ssh-entrypoint: kill: (72) - No such process
hacker@processes~killing-processes:~$ kill 96
ssh-entrypoint: kill: (96) - No such process
hacker@processes~killing-processes:~$ kill 76
hacker@processes~killing-processes:~$ kill 74
ssh-entrypoint: kill: (74) - No such process
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{UxAOZzR6G460EUdClx7xpwpSWGE.dJDN4QDLxMTO0czW}
hacker@processes~killing-processes:~$
```
Finally after a lot of trials and errors, I could finally get the flag. I wasnt realizing that after giving the kill command, I had to enter /challenge/run too.
