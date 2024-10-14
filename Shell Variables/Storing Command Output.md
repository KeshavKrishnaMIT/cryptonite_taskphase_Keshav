# Storing Command Output
```bash
Connected!
hacker@variables~storing-command-output:~$ PWN=$(cat /PWN)
cat: /PWN: No such file or directory
hacker@variables~storing-command-output:~$ cat PWN
COLLEGE
hacker@variables~storing-command-output:~$ echo "$COLLEGE"

hacker@variables~storing-command-output:~$ ^C
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{YwyNoBA6hgQRgOCTIX0t9XqPPNp.dVzN0UDLxMTO0czW}
hacker@variables~storing-command-output:~$
```
Writing PWN=$(/challenge/run) at first seemed a bit weird, so I tried different alternatives, but on reading the challenge properly, I realised that I was on the right path.
