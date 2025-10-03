### Adding Commands 

Previously, the `win` command that `/challenge/run` executed was stored in `/challenge/more_commands`. This time, `win` does not exist! Recall the final level of [Chaining Commands](https://pwn.college/linux-luminarium/chaining), and make a shell script called `win`, add its location to the `PATH`, and enable `/challenge/run` to find it!

**flag:** `pwn.college{4_-m6mkOysVhNXcVRWit3mnlcNr.QX2cjM1wyNwkzNyEzW}`

Commands used:

`touch /tmp/win`

`echo "cat /flag" > /tmp/win`

`chmod +x /tmp/win`

`export PATH="/tmp:$PATH`

`/challenge/run`

Breakdown: 
- `touch /tmp/win` -> creates a file win in the tmp directory 
- `echo "cat /flag" -> /tmp/win` wrote the output of the echo command to the created file 
- `chmod +x /tmp/win` -> made the file executable
- `export PATH="/tmp:$PATH"` -> Added the directory `/tmp` to the PATH variable.
- Ran `/challenge/run` to get the flag. 