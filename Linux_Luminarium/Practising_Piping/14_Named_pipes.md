### Named pipes 

This challenge will be a simple introduction to FIFOs. You'll need to create a `/tmp/flag_fifo` file and redirect the stdout of `/challenge/run` to it. If you're successful, `/challenge/run` will write the flag into the fifo! Go do it!

Basically, operations on FIFOs will *block* until both the read side and the write side is open, so `/challenge/run` will not actually be launched until you start reading from the FIFO. 
So, simultaneously, `cat /tmp/flag_fifo` and `/challenge/run > /tmp/flag_fifo` need to be run. 

Command used: 
`mkfifo /tmp/flag_fifo`
`cat /tmp/flag_fifo &`<- & will put the cat command in the background
`/challenge/run > /tmp/flag_fifo`


flag: `pwn.college{ED2dL7wmKZw1oqjcxW_ICbCqcLo.01MzMDOxwyNwkzNyEzW}`