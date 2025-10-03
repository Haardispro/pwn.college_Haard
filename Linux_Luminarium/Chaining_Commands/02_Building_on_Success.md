### Building on Success 

In this challenge, you need to chain the programs `/challenge/first-success` and `/challenge/second` using the `&&` operator. Try running each command separately first to see what happens (which is that you will _not_ get the flag). But if you chain them with `&&`, the flag will appear!

**flag:** `pwn.college{sl6rM-iBNmbDSyQTBoCdgzdGowP.0lM0MDOxwyNwkzNyEzW}`

Command used:
`/challenge/first-success && /challenge/second`

When I ran the commands individually, I didn't get the flag as per the instructions. But when I chained them together with the `&&` operator I got the flag.

Basically `&&` only allows you to run a second command if the first command succeeds(meaning exit 0). 

