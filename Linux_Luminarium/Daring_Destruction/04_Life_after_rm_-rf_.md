### Life after rm -rf / 

This challenge will force you to try it. It's almost the same as the previous one, but you must read the flag yourself after you destroy the system. After you `rm` everything, your previously-launched `/challenge/check` will restore the `/flag` file and make it readable. Then you can `read` it!

**flag:** `pwn.college{IxtJhQeHp7qyHxQaCFAGuWr5GjZ.01MzEzNxwyNwkzNyEzW}`

What I did: 
I split terminal into two windows using `tmux`, ran `rm -rf / --no-preserve-root` in 1st window and second window I ran `/challenge/check`


I ran this script to find the contents of the `/flag`:
```bash
while read line; do
    echo "Line: $line"
done < /flag
```

This script runs a while loop, which reads the variable line and prints out the variable using the echo command. The `read` command takes in input from the file `/flag` instead of `stdin`
