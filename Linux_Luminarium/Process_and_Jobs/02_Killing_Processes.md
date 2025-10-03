### Killing Processes 

Now, it's time to terminate your first process! In this challenge, `/challenge/run` will refuse to run while `/challenge/dont_run` is running! You must find the `dont_run` process and `kill` it. If you fail, `pwn.college` will disavow all knowledge of your mission. Good luck.

Command used: 
`ps -ef`
`kill 128`

flag: `pwn.college{AJ66-q1fb_D4qZJzN4kCgZrpuFq.QXyQDO0wyNwkzNyEzW}`

We need to pass in the `PID` -> Process Identifier of a given process as an argument to the `kill` command to stop that process from running.

