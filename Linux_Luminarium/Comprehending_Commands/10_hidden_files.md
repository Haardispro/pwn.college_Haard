### hidden files 

Interestingly, `ls` doesn't list _all_ the files by default. Linux has a convention where files that start with a `.` don't show up by default in `ls` and in a few other contexts. To view them with `ls`, you need to invoke `ls` with the `-a` flag, as so:

```console
hacker@dojo:~$ touch pwn
hacker@dojo:~$ touch .college
hacker@dojo:~$ ls
pwn
hacker@dojo:~$ ls -a
.college	pwn
hacker@dojo:~$
```

Now, it's your turn! Go find the flag, hidden as a dot-prepended file in `/`.

**Flag:** `pwn.college{gvDOZEs8efj52MNd2a9BfOsODDu.QXwUDO0wyNwkzNyEzW}`

commands used: 
`cd /`
`ls -a`
`cat .flag-31368749318170`

Moved to the root directory using the `cd`  command and looked for the `.` prepended file using `ls -a` which lists all files in the present working directory along with the hidden files. 
Read the flag using the `cat` command. 

