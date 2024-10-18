# Executable Files
```bash
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jul  4 06:37 /challenge/run
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{st0xL-lkPU5C9n5B-JFztgYIi9e.dJTM2QDLxMTO0czW}
hacker@permissions~executable-files:~$
```
Changed the permission so that file can be executed by the user using chmod u+x and then the user can easily execute the program.
