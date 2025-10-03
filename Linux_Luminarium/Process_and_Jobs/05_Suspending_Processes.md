### Suspending Processes

This level's `run` wants to see another copy of itself running _and using the same terminal_. How? Use the terminal to launch it, then suspend it, then launch another copy while the first is suspended!

**flag:** `pwn.college{ERp1c9-k62BeVLKphALYa_XzG9w.QX1QDO0wyNwkzNyEzW}`

Commands used: 
`/challenge/run`
`Ctrl-Z`
`/challenge/run`


`Ctrl-Z` suspends a running program in the background. Here, this level's `run` wants to see another copy of it running and using the same terminal, so I ran the command again to make another copy of it. 