### Understanding Shebangs

For this challenge, create a script at `/home/hacker/solve.sh` that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run `/challenge/run` to verify your script works correctly!

**flag:** `pwn.college{MnSNin5dCrWHTdtpr7zRh4qq45l.0VOzMDOxwyNwkzNyEzW}`

solve.sh
```bash
#!/bin/bash
echo "hack the planet"
```
Command used: 
`chmod +x solve.sh`
`/challenge/run`

#### What I learnt: 
When `./script.sh` was executed, Linux opened the file, read the first line, extracted `/bin/bash` as the interpreter, and executed `/bin/bash ./script.sh` to launch the script!
- `#!/bin/bash` for bash scripts
- `#!/usr/bin/python3` for Python scripts
- `#!/bin/sh` for POSIX shell scripts --- this is a more primitive predecessor to `bash` with fewer features, but more compatibility to non-Linux systems!


