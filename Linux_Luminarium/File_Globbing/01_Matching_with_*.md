### Matching with *

Now, practice this yourself! Starting from your home directory, change your directory to `/challenge`, but use globbing to keep the argument you pass to `cd` to at most four characters! Once you're there, run `/challenge/run` for the flag!


**flag:** `pwn.college{YwT4dpamDPTSAT0uW3QPhxzbuNb.QXxIDO0wyNwkzNyEzW}`

Command used: 
`cd /ch*`
`/challenge/run`

I had to change my directory to `/challenge` but according to the condition I cannot use more than 4 characters. Therefore, I used the command `cd /ch*`, `*` matches everything after previously passed characters. 
After changing directories, I ran `/challenge/run` to obtain the flag. 

