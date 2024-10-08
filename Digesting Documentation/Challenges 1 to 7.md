# Challenge 1: Learning from Documentation
```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is the /flag file:
pwn.college{k9TI9IS6ZvpZ4GOhrBicj7t9OL5.dZDN1QDLxMTO0czW}
```

# Challenge 2: Learning Complex Usage
```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{sT0Ps51UpSE-34If_EEgHWuEUdm.dVjM5QDLxMTO0czW}
```

# Challenge 5: Searching For Manuals
```bash
Connected!
hacker@man~searching-for-manuals:~$ man -k /challenge/challenge
nzyjkcjtqd (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man nzyjkcjtqd

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --nzyjkc NUM
              print the flag if NUM is 047

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                            May 2024                                          CHALLENGE(1)
hacker@man~searching-for-manuals:~$ /challenge/challenge -nzyjkc 047
Incorrect usage! Please read the challenge man page!
hacker@man~searching-for-manuals:~$ /challenge/challenge --nzyjkc 047
Correct usage! Your flag: pwn.college{0B4VSnzGGMyM7jGkM7LFcQPZjtq.dZTM4QDLxMTO0czW}
```

# Challenge 3: Reading Manuals
```bash
Connected!
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --oqxeys NUM
              print the flag if NUM is 650

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                            May 2024                                          CHALLENGE(1)
hacker@man~reading-manuals:~$ challenge --oqxeys 650
ssh-entrypoint: challenge: command not found
hacker@man~reading-manuals:~$ /challenge/challenge --oqxeys 650
Correct usage! Your flag: pwn.college{Yo6A5qTxe0Jy1sY3NxylKtnC8cr.dRTM4QDLxMTO0czW}
hacker@man~reading-manuals:~$
```

# Challenge 6: Helpful Programs
```bash
root@ZEROBOOK13:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 140
hacker@man~helpful-programs:~$ /challenge/challenge -g 140
Correct usage! Your flag: pwn.college{Q-DnHSC1brQSjWgLPDkeDcAiYwf.ddjM4QDLxMTO0czW}
hacker@man~helpful-programs:~$
```

# Challenge 7: Help for Builtins
```bash
Connected!
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "068EFzGA".
hacker@man~help-for-builtins:~$ challenge --secret "068EFzGA"
Correct! Here is your flag!
pwn.college{068EFzGA2jgI05UBp4Sbvgamyzt.dRTM5QDLxMTO0czW}
```



