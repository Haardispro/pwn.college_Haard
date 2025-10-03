### Finding Sessions 

In this challenge, we've created three screen sessions for you. One of them contains the flag. The other two are decoys!

**flag:** `pwn.college{8SsSAMp-ssAEC9Oln725cRXpICn.01N4IDOxwyNwkzNyEzW}`

Command used: 

 `screen -ls`

`screen -r {session_name}`

What did I do: 

- `screen -ls` -> lists all the screen session which are actively running.
```
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        145.session_690224cce40a268f    (Detached)
        148.session_d8e95c802ba7568a    (Detached)
        151.session_7973869ffdbf2dc6    (Detached)
3 Sockets in /home/hacker/.screen.
```

- `screen -r 145.session_690224cce40a268f` 
- I checked every session, but I found the flag in the first session only. 


