# The path variable
```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{4HCk5LMrfU2zLU5xqQOO8TVzMS8.dZzNwUDLxMTO0czW}
```
By setting the value yo nothing, PATH can not locate where the command is stored.
