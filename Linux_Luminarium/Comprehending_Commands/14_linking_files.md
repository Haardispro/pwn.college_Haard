### linking files 

Okay, now you try it! In this level the flag is, as always, in `/flag`, but `/challenge/catflag` will instead read out `/home/hacker/not-the-flag`. Use the symlink, and fool it into giving you the flag!


**Flag:** `pwn.college{YQLFN3_3SObpSUHQ4D0Y1bVSY4E.QX5ETN1wyNwkzNyEzW}`

Command used: 
`ln -s /flag /home/hacker/not-the-flag`
`/challenge/catflag`


`ln -s` creates a symbolic link to a given source file
This is how it works: 
- `ln -s <source> <destination>`
Here, `/challenge/catflag` will only read out `/home/hacker/not-the-flag`, therefore I need to make a symlink to `/flag`. Using the above commands I did just that. I used `/challenge/catflag` to output me the required flag. 

#### What I learnt: 

In a filesystem, a file is, conceptually, an address at which the contents of that file live. A hard link is an alternate address that indexes that data --- accesses to the hard link and accesses to the original file are completely identical, in that they immediately yield the necessary data. A soft/symbolic link, instead, contains the original file name. When you access the symbolic link, Linux will realize that it is a symbolic link, read the original file name, and then (typically) automatically access that file. In most cases, both situations result in accessing the original data, but the mechanisms are different.