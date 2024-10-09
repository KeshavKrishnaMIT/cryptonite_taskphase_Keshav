# Redirecting Output
```bash
Connected!
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{46cI0BsV96cspFynuaVEycoBnBW.dRjN1QDLxMTO0czW}
hacker@piping~redirecting-output:~$
```
To get PWN as output, used echo command, and to redirect PWN to COLLEGE file used >

# Redirecting more output
```bash
Connected!
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{sfeH1ekZGbIwfpBMh_Nga2EMGN9.dVjN1QDLxMTO0czW}

hacker@piping~redirecting-more-output:~$
```
Followed the same procedure as first challenge, and after redirecting the output to the file, used cat commmand to read the contents.

# Appending Output

```bash
Connected!
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{o4F6B6P7S4lwDdh5chWSaUlf7SQ.ddDM5QDLxMTO0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$
```
Use >> instead of > to append the output.

# Redirecting Errors
```bash
Connected!
hacker@piping~redirecting-errors:~$ /challenge/run >myflag 2>instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{sJBMMhRvF-BFl36GlzMFfP03Ck3.ddjN1QDLxMTO0czW}

hacker@piping~redirecting-errors:~$
```
The challenge asked to use > and 2> together.

# Redirecting Input
```bash
Connected!
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{wLcxtWCTt63_td0Z3NRt26y13fp.dBzN1QDLxMTO0czW}
hacker@piping~redirecting-input:~$
```
Redirected the output college to file PWN using > and then redirected the input of PWN to /challenge/run using <.

# Grepping Stored Results
```bash
Connected!
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college{ /tmp/data.txt
pwn.college{Ik2LNicRju4g4OzHoPt6b1FGIHD.dhTM4QDLxMTO0czW}
hacker@piping~grepping-stored-results:~$
```
First store the outputby redirecting it to /tmp/data.txt,, Then as we know every flag begins with pwn.college, so I found it using grep,, and at the end we needed to find it in in the output which was already stored in the file.

# Grepping Live Output
```bash
root@ZEROBOOK13:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{41QLjtIXXfjcmZzIucJPiuu3F2G.dlTM4QDLxMTO0czW}
hacker@piping~grepping-live-output:~$
```

# Grepping Errors
```bash
Connected!
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{YYgtoddHSVgyg-Xv01EMmvRk2Bp.dVDM5QDLxMTO0czW}
hacker@piping~grepping-errors:~$
```
# Duplicating Piped Data With Tee
```bash
root@ZEROBOOK13:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn |/challenge/college
Processing...
WARNING: you are overwriting file pwn with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "4dRpiHkc"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "4dRpiHkc" | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{4dRpiHkcmxP9Lpyl1yS_RSZdpJJ.dFjM5QDLxMTO0czW}
hacker@piping~duplicating-piped-data-with-tee:~$
```

Used tee pwn to store the output in pwn file, then used cat command to retrieve the secret code and at last used the secret code and piped it to /challenge/college to get the flag.

# Writing to multiple programs
```bash
Connected!
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2595413176376018427

Are you sure you're properly redirecting input into '/challenge/planet'?
Are you sure you're properly redirecting input into '/challenge/the'?
hacker@piping~writing-to-multiple-programs:~$
```
Dont know what to do next, I am stuck.

# Split Piping Stderr and Stdout
```bash
Connected!
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >( /challenge/the ) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{kJn_vpBnuVZuXiGcRkSjPLjFj5a.dFDNwYDLxMTO0czW}
hacker@piping~split-piping-stderr-and-stdout:~$
```
There is an alternative way too, to use > > but I used pip | for /challenge/planet.
