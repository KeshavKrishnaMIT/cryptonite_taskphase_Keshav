# Reading Files
```bash
Connected!
hacker@variables~reading-files:~$ read /challenge/read_me
You invoked 'read', but it looks like you didn't specify the PWN variable! You
will need to read the input into the PWN variable to pass this level.
ssh-entrypoint: read: `/challenge/read_me': not a valid identifier
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{MD5R8tc4GGaTw4nil9qMJRFD5ze.dBjM4QDLxMTO0czW}
hacker@variables~reading-files:~$
```
Again, followed the challenge description and got the output after commiting a small mistake in the first try.
