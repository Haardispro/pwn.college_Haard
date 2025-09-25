### Reading Manuals 

The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for `challenge`!


flag: `pwn.college{Ydl8lofaju2uZvt8Gol1cwP96TL.QX0EDO0wyNwkzNyEzW}`

Commands used: 
`man challenge`
`/challenge/challenge --dllofa 828`

I looked up the manual page for the program `challenge`. 
This is what it gave me: 
```bash 
> /challenge/bin/man challenge
"CHALLENGE(1)                                            Challenge Commands                                           CHALLENGE(1)

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

       --dllofa NUM
              print the flag if NUM is 828"
```

In the manual page its written clearly that `/challenge/challenge` will only give out the flag if passed withe the argument `--dllofa 828`, I did that and got the flag. 