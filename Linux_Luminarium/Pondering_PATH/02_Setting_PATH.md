### Setting PATH 

This level's `/challenge/run` will run the `win` command via its bare name, but this command exists in the `/challenge/more_commands/` directory, which is not initially in the PATH. The `win` command is the _only_ thing that `/challenge/run` needs, so you can just overwrite `PATH` with that one directory. Good luck!

**flag:** `pwn.college{YhFfJxQadk3g8fb7fGikLScTiNm.QX1cjM1wyNwkzNyEzW}`

Command used:

`export PATH=$PATH:/challenge/more_commands`

`/challenge/run`

Breakdown: 

- `export PATH=$PATH:/challenge/more_commands` -> I used this command to append the directory `/challenge/more_commands` to the `PATH` variable. I didn't want to wipe out every other command by just using `export PATH=/challenge/more_commands` because I may need the other commands if I mess up something. 
- Ran `/challenge/run` to get the flag. 
