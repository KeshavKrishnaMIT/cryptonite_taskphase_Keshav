# Home Swweet Home

```bash
hacker@paths~home-sweet-home:~$ /challenge/run /a
The argument you provided is not under your home directory!
hacker@paths~home-sweet-home:~$ /home/hacker/a
ssh-entrypoint: /home/hacker/a: No such file or directory
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{YAY2VMJggBKXCASI4IUsoURWj2I.dNzM4QDLxMTO0czW}
```

So reading the description provided in the challenge description, I tried a few things, and I figured out that to open the home directory, I have to use ~/ thing and I got the flag!!!
