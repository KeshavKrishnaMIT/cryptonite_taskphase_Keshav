# Backgrounding Processes
```bash
Connected!
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          83 S+   bash /challenge/run
root          85 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.
hacker@processes~backgrounding-processes:~$
hacker@processes~backgrounding-processes:~$
hacker@processes~backgrounding-processes:~$
hacker@processes~backgrounding-processes:~$
hacker@processes~backgrounding-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.0   1056   640 ?        Ss   14:14   0:00 /sbin/doc
root           7  0.0  0.0   5052  2240 ?        S    14:14   0:00 /run/dojo
hacker        66  0.1  0.0   5372  4160 pts/0    Ss   14:14   0:00 /run/dojo
root          83  0.0  0.0   5788  2880 pts/0    S    14:14   0:00 bash /cha
root          93  0.0  0.0   4268  1600 pts/0    S    14:15   0:00 sleep 6h
hacker        94  0.0  0.0   7868  3520 pts/0    R+   14:15   0:00 ps aux
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          83 S    bash /challenge/run
root          93 S    sleep 6h
root          95 S+   bash /challenge/run
root          97 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{McHb2y9nctC51wIryvmCPlWItN4.ddDN4QDLxMTO0czW}
```

This could have gotten a bit before but I got confused due to some extra information given. Overall the challenge was simple, after entering bg command for letting it resume in the background, I just had to enter run the command for one more time but I mistakingly went to ps aux. Happens!
