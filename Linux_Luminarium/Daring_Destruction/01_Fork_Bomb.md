### Fork Bomb

This challenge contains a `/challenge/check` that'll try to determine if your fork bomb is working (e.g., if it can't launch new processes) and give you the flag if so. Make sure to launch it (in a different terminal) _before_ launching your attack; otherwise you won't be able to launch it!

**flag:** `pwn.college{AUvJKuYf3E-BdcITvNFbR17YszP.0VMyEzNxwyNwkzNyEzW}`

fork contains:
```bash
#!/bin/bash
:(){ :|:& };:
```

I did know there is something like a fork bomb, but didn't know the exact syntax for it. So I had to lookup how its written. 

### What I learnt 

A fork bomb is a denial-of-service attack. Its a piece of code that causes a process to replicate, and each time, the new instance of the program further depletes available resources. When its run a computer, it just crashes. 

Breakdown of the command:  

| Symbol    | Meaning                                  |
| --------- | ---------------------------------------- |
| `:`       | Function name                            |
| `()`      | Defines the function                     |
| `{ ... }` | Function body                            |
| `&`       | Run in background                        |
| `; :`     | Call the function once to start the bomb |
