### Finding meaning after rm -rf / 

Whatever route you use, find the randomly-named file that `/challenge/check` makes in `/` after you `rm`, read it, and get the flag!

What I did: 
I split terminal into two windows using `tmux`, ran `rm -rf / --no-preserve-root` in 1st window and second window I ran `/challenge/check`

Command used: 
`echo /*`

I ran this script to find the contents of the `/flag`:
```bash
while read line; do
    echo "Line: $line"
done < /aa93cccf
```



