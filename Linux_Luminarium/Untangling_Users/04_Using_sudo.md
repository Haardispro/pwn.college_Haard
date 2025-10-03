### Using sudo 

In this level, we will give you `sudo` access, and you will use it to read the flag. Nice and easy!

**flag:** `pwn.college{QfI55yhBLdABlmG_h9yJtjl4Q7I.QX4UDN1wyNwkzNyEzW}`

Commands used: 
`cd /`
`sudo cat flag`

Changed to the root directory and read the flag using `sudo`.  
#### What I learnt: 
Unlike `su`, which relies on password authentication, `sudo` checks policies to determine whether the user is authorized to run commands as `root`. These policies are defined in `/etc/sudoers`, and though it's mostly out of scale for our purposes, there are plenty of [resources](https://www.digitalocean.com/community/tutorials/how-to-edit-the-sudoers-file) for learning about this!