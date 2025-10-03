### Scripting with Arguments
For this challenge, you need to write a script at `/home/hacker/solve.sh` that:

1. Takes two arguments
2. Outputs them in REVERSE order (second argument first, then the first argument)

For example:

```console
hacker@dojo:~$ bash /home/hacker/solve.sh pwn college
college pwn
hacker@dojo:~$
```
Once your script works correctly, run `/challenge/run` to get your flag!

**flag:** `pwn.college{IgsOAwEmhqCCOiG7ZyvhFABiIsn.0VNzMDOxwyNwkzNyEzW}`


Command used: 
`bash solve.sh pwn college`
`/challenge/run`
Followed the instructions to create this file: 
solve.sh 
```bash
echo "$2 $1"
```

$ would be taken as an argument in the shell.

