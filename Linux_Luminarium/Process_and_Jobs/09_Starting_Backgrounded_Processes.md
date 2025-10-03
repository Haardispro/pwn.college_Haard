### Starting Backgrounded Processes

Here, `sleep` is actively running in the background, _not_ suspended. Now it's your turn to practice! Launch `/challenge/run` backgrounded for the flag!

**flag:** `pwn.college{Y-aFF-j3MRXSOQ6hflqX467gR7o.QX5QDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run`
`/challenge/run &`

This is what I did: 
```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run
You've started me in the foreground! You must start me in the background (by 
appending '&' to the command) to get the flag!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run & 
[1] 147
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{Y-aFF-j3MRXSOQ6hflqX467gR7o.QX5QDO0wyNwkzNyEzW}
```

