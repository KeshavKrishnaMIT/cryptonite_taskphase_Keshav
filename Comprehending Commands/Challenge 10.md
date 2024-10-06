# Making directories
```bash 
Connected!
hacker@commands~making-directories:~$ mkdir tmp/pwn
mkdir: cannot create directory ‘tmp/pwn’: No such file or directory
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ ls
Desktop  a
hacker@commands~making-directories:~$ ls /tmp/pwn
college
hacker@commands~making-directories:~$ / challenge/run
ssh-entrypoint: /: Is a directory
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{Iyv1f-4UIssQK2MmbejrCeGHXmV.dFzM4QDLxMTO0czW}
```

A few errors initaially, but got it in the end.
