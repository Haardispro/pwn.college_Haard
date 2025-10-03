### Redirecting Script Output

In this level, we will practice piping (`|`) from your script to another program. Like before, you need to create a script that calls the `/challenge/pwn` command followed by the `/challenge/college` command, and pipe the output of the script into a single invocation of the `/challenge/solve` command!

**flag:** `pwn.college{YMMgsoosi3zCjCXkzqomESHxYWU.QX4ETO0wyNwkzNyEzW}`

Command used: `bash x.sh | /challenge/solve`

x.sh: 
```bash
/challenge/pwn ; /challenge/college 
```

Using my knowledge from previous programs I piped the output of `x.sh` to `/challenge/solve` to get the flag.

