# Matching with *
```bash
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{gzUbRk6zWNcL3Mm436MHXRwEUgD.dFjM4QDLxMTO0czW}
hacker@globbing~matching-with-:/challenge$
hacker@globbing~matching-with-:/challenge$
```

# Matching with ?
```bash
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge$ ./run
ssh-entrypoint: /challenge$: No such file or directory
hacker@globbing~matching-with-:/challenge$ ./run./run./
ssh-entrypoint: ./run./run./: No such file or directory
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EvFZ349CGH99r4gTPBt9YmgVKjd.dJjM4QDLxMTO0czW}
```

# Matching with[]
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{Y7X6MWZ8FFYKgQ0_kzBh1bN9Zjk.dNjM4QDLxMTO0czW}
hacker@globbing~matching-with-:/challenge/files$
```

# Matching paths with []
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[abhs]
You got it! Here is your flag!
pwn.college{cqKY5yqT_4TkOiijrVnV45FAxpk.dRjM4QDLxMTO0czW}
```

# Mixing globs
```bash
Connected!
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{wNpv7s391DXjev5FXKTq3WjuCSF.dVjM4QDLxMTO0czW}
```

# Exclusionary Globbing
```bash
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful
challenging delightful educational fantastic great happy incredible jovial kind
laughing magical optimistic queenly radiant splendid thrilling uplifting
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{Yb_SvhMFp_STUBGksj7K9g-Dsuj.dZjM4QDLxMTO0czW}
hacker@globbing~exclusionary-globbing:/challenge/files$
```
