# Hidden Files

```bash
Connected!
hacker@commands~hidden-files:~$ ls -a
.   .ICEauthority  .bash_logout  .cache   .dbus   .profile  Desktop  a             linked-flag  not-the-flag  temp-flag
..  .bash_history  .bashrc       .config  .local  COLLEGE   PWN      instructions  myflag       pwn           the-flag
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-20545237439630  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ / .flag-20545237439630
ssh-entrypoint: /: Is a directory
hacker@commands~hidden-files:~$ cat / .flag-20545237439630
cat: /: Is a directory
cat: .flag-20545237439630: No such file or directory
hacker@commands~hidden-files:~$ cat /.flag-20545237439630
pwn.college{AoIpUewIbyXGFB-qEBAWEA-V2l_.dBTN4QDLxMTO0czW}
hacker@commands~hidden-files:~$
```

Followed whatever the challenge says.
