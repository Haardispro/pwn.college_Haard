### The PATH Variable

In this level, you will disrupt the operation of the `/challenge/run` program. This program will **DELETE** the flag file using the `rm` command. However, if it can't find the `rm` command, the flag will not be deleted, and the challenge will give it to you! Thus, you must make it so that `/challenge/run` also can't find the `rm` command!

**flag:** `pwn.college{8NuDy-Srp8-9ndqVLF87fat04h0.QX2cDM1wyNwkzNyEzW}`

Command used: 

`PATH=""`

`/challenge/run`

The `PATH` variable contains the path of the inbuilt binaries like `rm`, `cat` etc. But removing it won't allow you to use any binaries. 

So, the command `/challenge/run` won't be able to access the `rm` command, and then outputs the flag when run .  