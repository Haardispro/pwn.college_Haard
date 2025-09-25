### Helpful Programs: 

Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually, this argument is `--help`, but it can often be `-h` or, in rare cases, `-?`, `help`, or other esoteric values like `/?` (though that latter is more frequently encountered on Windows).

In this level, you will practice reading a program's documentation with `--help`. Try it out!

flag: `pwn.college{4jsMhsuwN8e-wZA5v4R2L2uQvI5.QX3IDO0wyNwkzNyEzW}`

Commands used: 
`/challenge/challenge --help`
`/challenge/challenge -p #to print out the secret value`
`/challenge/challenge --give-the-flag 485`

Passed the `--help` argument to `/challenge/challenge` to look at the docs. This was my workflow: 
```bash
> /challenge/challenge/ --help 
"usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag"
> /challenge/challenge -p 
"The secret value is: 485"
> /challenge/challenge -g 485
Correct usage! Your flag: pwn.college{4jsMhsuwN8e-wZA5v4R2L2uQvI5.QX3IDO0wyNwkzNyEzW}
```
