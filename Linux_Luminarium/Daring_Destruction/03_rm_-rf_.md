### rm -rf / 

In this challenge, you will do something that you might never do again: wipe the whole system. We've actually modified things a bit to keep your home directory safe (normally, it would get wiped as well!), but otherwise, all that stands before you and the flag is your willingness to wipe the drive. But before you wipe it all, make sure to start `/challenge/check` so that it can watch the fireworks (and give you the flag)!

What I did: 
I split terminal into two windows using `tmux`, ran `rm -rf / --no-preserve-root` in 1st window and second window I ran `/challenge/check`


flag: `pwn.college{IWUKZB38AlJU--tU64jBQ0AvRcj.0lMzEzNxwyNwkzNyEzW}`

