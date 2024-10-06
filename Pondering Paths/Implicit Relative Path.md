# Implicit Relative Path

```bash
hacker@paths~implicit-relative-path:/challenge$ .run
ssh-entrypoint: .run: command not found
hacker@paths~implicit-relative-path:/challenge$ /.run
ssh-entrypoint: /.run: No such file or directory
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sDmBnEazx46Wd8QuWSUTVWbuTXt.dFTN1QDLxMTO0czW}
```

So I ran different commands using different combinations of . and / and I got successful in my third attempt.
