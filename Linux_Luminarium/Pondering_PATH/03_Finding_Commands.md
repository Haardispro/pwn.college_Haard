### Finding Commands 

In this challenge, we added a `win` command somewhere in your `$PATH`, but it won't give you the flag. Instead, it's in the same directory as a `flag` file that we made readable by you! You must find `win` (with the `which` command), and `cat` the flag out of that directory!

**flag:** `pwn.college{ACHDGuUNrvums7psBlQRBowVQXD.01NzEzNxwyNwkzNyEzW}`

Commands used:

`which win`

`cd /challenge/paths/19500`

`cat flag`

The `which` command is used to locate a given shell command in the file system.
I used it to find the directory of the command `win`. I found it and changed my directory to the given path and read the flag.

