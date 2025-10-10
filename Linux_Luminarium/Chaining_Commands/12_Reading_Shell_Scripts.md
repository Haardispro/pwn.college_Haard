In this level, we will learn to read shell scripts. /challenge/run is a shell script that requires you to put in a secret password, but that password is hardcoded into the script iself! Read the script (using, say, cat), figure out the password, and get the flag!

**flag:** `pwn.college{gAXPGX8XLlbomoVF2h853vcqHmb.0lMwgDOxwyNwkzNyEzW}`


What I did: 
- ran `cat /challenge/run` to view the contents of the given file. 
``` bash 
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
```

The code is self explanatory. 
The code takes input into a variable called `GUESS`. If the given input is `hack the PLANET`, then `cat /flag` will be executed. 

Subsequently, I ran `/challenge/run` and gave the required input to get the flag. 

```bash 
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{gAXPGX8XLlbomoVF2h853vcqHmb.0lMwgDOxwyNwkzNyEzW}
```

