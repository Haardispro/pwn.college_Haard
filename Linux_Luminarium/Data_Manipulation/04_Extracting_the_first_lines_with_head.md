### Extracting the first lines with head 

This challenge's `/challenge/pwn` outputs a bunch of data, and you'll need to pipe it through `head` to grab just the first 7 lines and then pipe them onwards to `/challenge/college`, which will give you the flag if you do this right! Your solution will be a long composite command with _two_ pipes connecting three commands. Good luck!

**flag:** `pwn.college{YVVMAZQ6yPDDrrTmhwj3QDU7JiF.0lNxEzNxwyNwkzNyEzW}`

Command used: 
`/challenge/pwn | head -n 7 | /challenge/college`


The `head` command gives you the initial values of the given output of a command. 

According to the challenge, I piped the values of `/challenge/pwn`  to head which extracted exactly 7 lines using `-n 7` argument and then piped the 7 lines to `/challenge/college` to get the flag. 
