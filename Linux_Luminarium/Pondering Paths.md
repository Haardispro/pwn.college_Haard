
### The root

Start the challenge, launch a terminal, invoke the `pwn` program using its absolute path, and Capture that Flag

--- 

**Flag:** `pwn.college{grhQeFLyB-F41zgl7AjoTSlPBqo.QX4cTO0wyNwkzNyEzW}`

command used: `/pwn`

Learnt what are absolute paths and passed in the above command to get the flag. 
### Program and absolute paths

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the `run` file that is in the `challenge` directory that is, in turn, in the `/` directory. If you invoke the challenge correctly, it will give you the flag.

--- 
**Flag:** `pwn.college{MXyaD9E5AMykE0MP-M0gzKTE4WO.QX1QTN0wyNwkzNyEzW}`

command used: `/challenge/run`

Used the knowledge of absolute file paths to pass the absolute file path of the `run` file to get the flag. 

### Position thy self 

This challenge will require you to execute the `/challenge/run` program from a specific path (which it will tell you). You'll need to `cd` to that directory before rerunning the challenge program. Good luck!

--- 
**Flag:** `pwn.college{AkKVGEkg5Fkua2F7vUZngxgRxyt.QX2QTN0wyNwkzNyEzW}`


command used: 
`cd /home`
`/challenge/run`

The program asked me to run `/challenge/run` from the `/home` directory, so I did that accordingly using the commands provided above. 

### Position elsewhere

This challenge will require you to execute the `/challenge/run` program from a specific path (which it will tell you). You'll need to `cd` to that directory before rerunning the challenge program. Good luck!

---
**Flag:** `pwn.college{IcsRKoqL735arUCQe43kyE6C6wZ.QX3QTN0wyNwkzNyEzW}`

command used: 
`cd /etc`
`/challenge/run`

### Position yet elsewhere

**Flag:** `pwn.college{gsFgajGIz-0Ryis3GoU0p5HFz-e.QX4QTN0wyNwkzNyEzW}`

command used: 
`cd /usr/aarch64-linux-gnu/include/gnu`
`/challenge/run`
### implicit relative paths, from /

Let's try it here! You'll need to run `/challenge/run` using a relative path while having a current working directory of `/`. For this level, I'll give you a hint. Your relative path starts with the letter `c` 

---
**Flag:** `pwn.college{Yh2unQjuafW4HQOWRlEFE-fnaHE.QX5QTN0wyNwkzNyEzW}`

command used: 
`cd /`
`challenge/run`
### explicit relative paths, from /

Of course, if your current working directory is `/`, the above relative paths are equivalent to the above absolute paths.

---
**Flag:** `pwn.college{QhS4qzh2IxHqQqyMCLLhWQhvuh7.QXwUTN0wyNwkzNyEzW}`

command used: 
`cd /`
`./challenge/run`
### implicit relative path 


**Flag:** `pwn.college{wS2wm3ciq1f4W-nYUGlVC3N-QEU.QXxUTN0wyNwkzNyEzW}`

command used: 
`cd /challenge`
`./run`
### home sweet home

**Flag:** `pwn.college{I81leMIiEDZR15X8NvsSH4IjDtE.QXzMDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run ~/h`


