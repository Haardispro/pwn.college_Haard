### Changing Permissions

In this challenge, you must change the permissions of the `/flag` file to read it! Typically, you need to have write access to the file in order to change its permissions, but I have made the `chmod` command all-powerful for this level, and you can `chmod` anything you want even though you are the `hacker` user. This is an ultimate power. The `/flag` file is owned by root, and you can't change that, but you can make it readable. Go and solve this!

**flag:** `pwn.college{YhCDf2Adf-d443dpWu69F9KJDQa.QXzcjM1wyNwkzNyEzW}`

Command used: 
`chmod +r /flag`
`cat /flag`

I used the `chmod` command to give read access to the file `/flag`. By default, if it isn't specified, read access will be given to all three user, group and world.



