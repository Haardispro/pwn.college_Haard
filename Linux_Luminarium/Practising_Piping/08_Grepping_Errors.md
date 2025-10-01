### Grepping Errors

Try it now! Like the last level, this level will overwhelm you with output, but this time on standard error. Grep through it to find the flag!

**flag:** `pwn.college{cBQnZD6sk8MqUyfJgLvtPcA9ECW.QX1ATO0wyNwkzNyEzW}`

Command used: 
`/challenge/run 2>& 1 | grep "pwn.college"`


The goal was to `grep` the error output of a program. Since the pipe (`|`) only works on standard output, I first redirected the standard error stream (FD 2) to the standard output stream (FD 1) using `2>&1`. Then, I piped this combined stream to `grep` to find the flag.