### more catting practice 

In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with `cd`, so no `cat flag` for you. You must retrieve the flag by absolute path, wherever it is.


**Flag:** `pwn.college{oofohlEVKeHHfDWYnYmiDOWCM3K.QXwITO0wyNwkzNyEzW}`

command used: `cat /usr/share/enchant-2/flag`

The challenge told me to look for the flag at `/usr/share/enchant-2/flag`, so I specified the absolute path of the flag and passed it as an argument to the `cat` command to obtain the flag.

#### What I learnt

You can pass absolute path as an argument in the `cat` command to read the contents of the given file. 