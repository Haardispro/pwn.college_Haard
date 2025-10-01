### Duplicating piped data with tee 

Now, you try it! This process' `/challenge/pwn` must be piped into `/challenge/college`, but you'll need to intercept the data to see what `pwn` needs from you!

**flag:** `pwn.college{0Xdh62afV6NYri9w0bJ8zYDE--f.QXxITO0wyNwkzNyEzW}`

Command used: 
Here `arg_file` can be any file text file, such as `pwn.txt` or `file.txt`. 

`/challenge/pwn | tee arg_file | /challenge/college`

`/challenge/pwn --secret 0Xdh62f | /challenge/college`

1. I first piped `/challenge/pwn` to `/challenge/college` and used `tee arg_file` to save the intermediate output. This initial attempt failed but captured the necessary debug info.
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee arg_file | /challenge/college
    Processing...
    The input to 'college' does not contain the correct secret code! This code
    should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
    output of 'pwn' and figure out what the code needs to be.
```

2. I then examined the saved output with `cat arg_file` and discovered that the `pwn` command required a secret argument: `--secret 0Xdh62f`
```
    hacker@piping~duplicating-piped-data-with-tee:~$ cat arg_file
    Usage: /challenge/pwn --secret [SECRET_ARG]
    
    SECRET_ARG should be "0Xdh62af"
```

3.  Finally, I ran the command again with the correct secret argument. This successfully piped the required data to `/challenge/college` and printed the flag.
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 0Xdh62af | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{0Xdh62afV6NYri9w0bJ8zYDE--f.QXxITO0wyNwkzNyEzW
```

#### What I learnt: 

I learnt how the **`tee`** command works like a T-splitter, duplicating a data stream. It passes data through to the next command in a pipe while also saving a copy to a file, which is extremely useful for debugging pipelines.
