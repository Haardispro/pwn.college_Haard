### Listing Processes 

Anyways! Let's practice. In this level, I have once again renamed `/challenge/run` to a random filename, and this time made it so that you cannot `ls` the `/challenge` directory! But I also launched it, so you can find it in the running process list, figure out the filename, and relaunch it directly for the flag! Good luck!

**flag:** `pwn.college{46NmO0UrBQJf9nsDGqO_yncPMNK.QX4MDO0wyNwkzNyEzW}`

Commands used: 
`ps -ef`
`/challenge/5818-run-13577`



I used the command `ps -ef` to list every process in full format. 
I found out which process contained the flag and ran it to get the flag.
 