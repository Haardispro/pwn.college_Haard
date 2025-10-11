### Finding meaning after rm -rf / 

Whatever route you use, find the randomly-named file that `/challenge/check` makes in `/` after you `rm`, read it, and get the flag!

**flag:** `pwn.college{practice}` 

What I did: 
I split terminal into two windows using `tmux`, ran `rm -rf / --no-preserve-root` in 1st window and second window I ran `/challenge/check`

Command used: 
- `echo /*` -> This command prints out all the files and directories in the root directory, can be used in the absence of `ls`.  

I ran this script to find the contents of the `/flag`:
```bash
while read line; do
    echo "Line: $line"
done < /aa93cccf
```

I had to look up how to write the script, but I do understand what it does.

Basically, the script runs a while loop, the `read` command reads one line at a time from the input, in this case `/aa93cccf`. 
The read line is stored in the variable `$line`.
`do..done` defines the loop body, the commands inside are executed for each line read. 
`< /aa93cccf` redirects the file `/aa93cccf` as the input to the `while` loop. 
So instead of reading from `stdin` the `read` command reads from the given file. 

 