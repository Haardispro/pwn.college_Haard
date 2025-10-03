### Groups and Files

In this level, I have made the flag readable by whatever group owns it, but this group is currently `root`. Luckily, I have also made it possible for you to invoke `chgrp` as the `hacker` user! Change the group ownership of the flag file, and read the flag!


**flag:** `pwn.college{QNDcOl_Uqroi2EEI2TfmZokfS-5.QXxcjM1wyNwkzNyEzW}`

Command used: 
`chgrp hacker /flag`
`cat /flag`

I changed the group ownership  of the `/flag` file and read it with `cat` to get the flag.
 
