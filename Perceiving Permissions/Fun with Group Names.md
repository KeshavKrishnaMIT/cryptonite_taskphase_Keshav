# Fun with group names
```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp14448) groups=1000(grp14448)
hacker@permissions~fun-with-groups-names:~$ ls -l / | grep flag
-r--r-----    1 root root   58 Oct 18 05:30 flag
hacker@permissions~fun-with-groups-names:~$ chgrp grp14448 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{0dmk5bJR8nmK0LI1n-B1sMLxnmk.dJzNyUDLxMTO0czW}
hacker@permissions~fun-with-groups-names:~$
```
Used id command to find the group initially the flag is in and then changed the group, read out the contents using the cat command.
