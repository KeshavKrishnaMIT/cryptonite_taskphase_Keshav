# Explicit relative paths

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge/.run/
ssh-entrypoint: challenge/.run/: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QsdPbXyWqdWVSRJx6H-AKhl26Xh.dBTN1QDLxMTO0czW}
hacker@paths~explicit-relative-paths-from-:/$
```

Changed the directory to / and then began with trying different relative paths given in the challenge and the second one worked.
