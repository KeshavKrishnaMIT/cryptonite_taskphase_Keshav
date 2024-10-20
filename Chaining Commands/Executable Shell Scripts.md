# Executable Shell Scripts
```bash
hacker@chaining~executable-shell-scripts:~$ echo "/challenge/solve" > script.sh
hacker@chaining~executable-shell-scripts:~$ ls -l script.sh
-rw-r--r-- 1 hacker hacker 17 Oct 20 15:02 script.sh
hacker@chaining~executable-shell-scripts:~$ chmod ugo+x ~/script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{cD-dm-G77kS_jwchCUQ3C-ZUVY-.dRzNyUDLxMTO0czW}
hacker@chaining~executable-shell-scripts:~$
```
Store the commands in a file called script.sh then change its permissions so that the file can be executed
