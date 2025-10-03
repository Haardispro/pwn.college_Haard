### Detaching and Attaching 

For this challenge, you'll need to:

1. Launch screen
2. Detach from it.
3. Run `/challenge/run` (this will secretly send the flag to your detached session!)
4. Reattach to see your prize

**flag:** `pwn.college{wK54H6F1R4PfWZljyjD1hKjyxeC.0lN4IDOxwyNwkzNyEzW}`

Commands used: 
`screen`

`CTRL + A, d`

`/challenge/run`

`screen -r`

Breakdown: 
- `screen` -> will start a screen session 
- `CTRL + A, d` -> Detaches a screen session and leaves the session running in the background while you return to your terminal 
- `/challenge/run` -> This will send the flag to the detached session 
- `screen -r` -> reattach the detached session 