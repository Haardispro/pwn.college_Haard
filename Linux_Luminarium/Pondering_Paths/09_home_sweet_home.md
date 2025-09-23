### home sweet home

**Flag:** `pwn.college{I81leMIiEDZR15X8NvsSH4IjDtE.QXzMDO0wyNwkzNyEzW}`

Command used: 
`touch h`

`/challenge/run ~/h`


`~` stands for the `/home/$USER/` directory. 
The challenged asked me the pass in an absolute path inside the home directory and the argument must be three characters or less. 

Therefore, I created a file `h` using the `touch` command and passed in the file with the absolute path as an argument to obtain the flag. 

The commands shown above were run in order to get the flag. 


