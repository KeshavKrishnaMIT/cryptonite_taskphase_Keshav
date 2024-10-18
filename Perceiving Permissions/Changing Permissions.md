# Changing Permissions
```bash
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 58 Oct 18 05:38 /flag
hacker@permissions~changing-permissions:~$ chmod go+r *
hacker@permissions~changing-permissions:~$ ls -l /flag
-r--r--r-- 1 root root 58 Oct 18 05:38 /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{Q_XNlE6YTyhnqZlT8LVr1JB6wO1.dNzNyUDLxMTO0czW}
hacker@permissions~changing-permissions:~$
```
Permission to read the contents of the flag is set only to the root user so I changed this setting using chmod and made it available for other also to read the file.
