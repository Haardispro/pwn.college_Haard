### Sniffing Process Arguments

That's what this challenge explores. Zardus is using an automation script, passing his account password to it as an argument. Zardus is also allowed to use `sudo` (and, thus, to `sudo cat /flag`!). Steal the password, log in to Zardus' account (recall the `su` command from the [Untangling Users](https://pwn.college/linux-luminarium/users) module), and get that flag!

**flag:** `pwn.college{U-jGB_TOoFV-8iwBF2JRvE49Nzs.0FOzEzNxwyNwkzNyEzW}`

Command used: 
- `ps aux`
- `password = pw_1680526469`
- `su zardus`
- `sudo cat /flag`


### What I learnt

The `ps aux` command displays all running processes on the system, for all users, including those without a controlling terminal in a detailed, user-friendly format.