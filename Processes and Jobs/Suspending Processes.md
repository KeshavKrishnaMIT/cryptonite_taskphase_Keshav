# Suspending Processes

```bash
Connected!
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 14:07 pts/0    00:00:00 bash /challenge/run
root          84      82  0 14:07 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 14:07 pts/0    00:00:00 bash /challenge/run
root          89      65  0 14:07 pts/0    00:00:00 bash /challenge/run
root          91      89  0 14:07 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{IjxN-t9XVZ1nkpse-ijXLJZhqku.dVDN4QDLxMTO0czW}
```

Just follow the challenge decription, once ctrl+z and then /challenge/run. Rest was done automatically.
