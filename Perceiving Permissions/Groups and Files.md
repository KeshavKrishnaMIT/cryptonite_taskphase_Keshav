# Groups and Files
```bash
hacker@permissions~groups-and-files:~$ ls -l / | grep flag
-r--r-----    1 root root   58 Oct 18 05:25 flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ ls -l / | grep flag
-r--r-----    1 root hacker   58 Oct 18 05:25 flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{8EWakyEFUjJcI_0KSqaPgeVz3sM.dFzNyUDLxMTO0czW}
hacker@permissions~groups-and-files:~$
```
We changed the group that owns the file and then we can access the flag.
