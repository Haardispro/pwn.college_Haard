### Becoming root with su 

But THIS challenge (and only this challenge) _does_ have a root password. That password is `hack-the-planet`, and you must provide it to `su` to become root! Go do that, and read the flag!

**flag:** `pwn.college{oDMDMrtR5ttdAazjju_cq6KIvFL.QX1UDN1wyNwkzNyEzW}`

Commands used: 
`su`
`cd /`
`cat flag`


The `su` command makes you the root user if you pass in the correct password. Which I did as it was given in the challenge description. 

Then I made my way to the root directory and read the flag, using the above mentioned commands.  