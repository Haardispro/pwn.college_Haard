### Fun With Groups Names

The point is, you've used `hacker` for the group before, but in this level, that is not going to work. I'll still allow you to use `chgrp`, but I have randomized the name of the group that your user is in. You will need to use the `id` command to figure that name out, then `chgrp` to victory!

**flag:** `pwn.college{s7vn16TUKOsy_A_rcIzU_Lr8k84.QXycjM1wyNwkzNyEzW}`

Commands used: 
`id`
`chgrp grp24801 /flag`
`cat /flag`


By using the `id` command I can look at which group the user, which is me is present in. 
I found it and used the `chgrp` command to change the group of `/flag`. I read the flag using `cat`. 

