### Executable Shell Scripts 

Try that here! Make a shell script that will invoke `/challenge/solve`, make it executable, and run it without explicitly invoking `bash`!

**flag:** `pwn.college{Ecc94E-4V6dPRwh-Id18EowMZsm.QX0cjM1wyNwkzNyEzW}`

Command used: 
`chmod +x x.sh`
`./x.sh`

I made a file x.sh which looks something like this: 

x.sh: 
```bash
#!/bin/bash
/challenge/solve
```

Made it executable, so I don't need to use bash to run it. Finally, ran `./x.sh` to get the flag. 



