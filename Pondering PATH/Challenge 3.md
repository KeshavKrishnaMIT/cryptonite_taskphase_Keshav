# Adding Commands
```bash
hacker@path~adding-commands:~$ echo "cat /flag" > win
hacker@path~adding-commands:~$ pwd
/home/hacker
hacker@path~adding-commands:~$ PATH=$PATH:/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/challenge/run: line 4: /home/hacker/win: Permission denied
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:~$ chmod ug+x /home/hacker/win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{gKrpL9Y1aVJv8LDiNV9-tK_azZY.dZzNyUDLxMTO0czW}
hacker@path~adding-commands:~$
```
Add the needed commands, then we need to add the path of win to PATH. Find the directry you stored win in and add the path of win to PATH.
Then change the permissions to be able to execute the file.
