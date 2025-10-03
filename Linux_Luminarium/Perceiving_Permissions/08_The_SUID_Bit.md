### The SUID Bit

Now, we are going to let you add the SUID bit to the `/challenge/getroot` program in order to spawn a root shell for you to `cat` the flag yourself!

**flag:** `pwn.college{w_5D30UErMwZAwfwR4e6VoH_-0r.QXzEjN0wyNwkzNyEzW}`

Command used: 
`chmod u+s /challenge/getroot`
`/challenge/getroot`
`cat /flag`

using the `u+s` argument adds the `SUID` bit to the user group. 
The "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's files. 

The `s` part in place of the executable bit means that the program is executable _with SUID_. It means that, regardless of what user runs the program (as long as they have executable permissions), the program will execute as the owner user (in this case, the `root` user).


