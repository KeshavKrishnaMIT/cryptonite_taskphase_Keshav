# Changing File Ownership
```bash
root@ZEROBOOK13:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@permissions~changing-file-ownership:~$ ls -l / | grep flag
-r--------    1 root root   58 Oct 15 18:28 flag
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l / | grep flag
-r--------    1 hacker root   58 Oct 15 18:28 flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{UvyCYsaEPnztTMMXuPT2gP0F9y4.dFTM2QDLxMTO0czW}
hacker@permissions~changing-file-ownership:~$
```

Change the ownership of the file using chown [username] [file] and then use ls -l | grep flag to show that the ownership was initially root and was then changed to user hacker...
