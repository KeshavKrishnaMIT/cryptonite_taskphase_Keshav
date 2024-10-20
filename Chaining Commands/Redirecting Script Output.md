# Redirecting Script Output
```bash
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn
> /challenge/college" > x.sh
hacker@chaining~redirecting-script-output:~$ cat x.sh
/challenge/pwn
/challenge/college
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{gdmSwfqeTrEt1R7Gkl24nYI9wh6.dhTM5QDLxMTO0czW}
hacker@chaining~redirecting-script-output:~$
```
Stored the commands in the file x.sh and then run the file using | to pip the output as input to /challenge.solve
