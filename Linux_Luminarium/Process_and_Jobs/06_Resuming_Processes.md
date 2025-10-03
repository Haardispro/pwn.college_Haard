### Resuming Processes

Go try it out! This challenge's `run` needs you to suspend it, then resume it. Good luck!

**flag:** `pwn.college{wVRZ_bmZxkjwn1gSujamd2Wd8XM.QX2QDO0wyNwkzNyEzW}`

Commands used: `/challenge/run`
`Ctrl-Z`
`fg`

To resume a  suspended program we use the `fg` command. I followed the instructions of the challenge and got the flag. 

#### What I learnt: 

To resume processes, your shell provides the `fg` command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.