# Listing Processes
```bash
Connected!
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  1.0  0.0   1056   640 ?        Ss   13:50   0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.2  0.0   5052  2240 ?        S    13:50   0:00 /run/dojo/bin/sleep 6h
root          68  0.0  0.0   4132  2560 ?        S    13:50   0:00 /challenge/6676-run-13167
root          72  0.0  0.0   2744  1280 ?        S    13:50   0:00 sleep 6h
hacker        73  1.0  0.0   5240  3840 pts/0    Ss   13:50   0:00 /run/dojo/bin/ssh-entrypoint
hacker        90  0.0  0.0   7868  3520 pts/0    R+   13:50   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/6676-run-13167
Yahaha, you found me! Here is your flag:
pwn.college{gt5CirH9AZRcsDlx60V23pdNcOb.dhzM4QDLxMTO0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```
Just entered ps aux(gut feeling, was also thinking of entering ps -ef initially) and then scanned through the output and got the flag.
