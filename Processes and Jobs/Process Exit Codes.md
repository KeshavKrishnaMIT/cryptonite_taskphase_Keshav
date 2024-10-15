# Process Exit Codes
```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
16
hacker@processes~process-exit-codes:~$ /challenge/submit-code 16
CORRECT! Here is your flag:pwn.college{gNzV-ZivvCNb1-MWBEfO4n8ClLr.dljN4UDLxMTO0czW}
```

To get the exit code in which program terminated with I ran it first, then used $? to get the code and then used the given exit code as an argument for /challenge/submit-code.
