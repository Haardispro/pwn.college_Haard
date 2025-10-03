### Printing Exported Variables

Try the `env` command: it'll print out every _exported_ variable set in your shell, and you can look through that output to find the `FLAG` variable!

**flag:** `pwn.college{sTklTp7hLyBWx-lBW0lRSnaBxRO.QX4UTN0wyNwkzNyEzW}`

Command used: `env | grep "FLAG"`

What I learnt is that the `env` command prints out every exported variable set in my shell. One of the variables was the flag, I used my knowledge from Practising Piping to grep the variable `FLAG` out of the output of the command `env`.