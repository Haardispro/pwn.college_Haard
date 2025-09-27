### Appending output

To practice, run `/challenge/run` with an append-mode redirect of the output to the file `/home/hacker/the-flag`. The practice will write the first half of the flag to the file, and the second half to `stdout` if `stdout` is redirected to the file. If you properly redirect in append-mode, the second half will be appended to the first, but if you redirect in _truncation_ mode (`>`), the second half will _overwrite_ the first and you won't get the flag!

Command used: 
`/challenge/run >> /home/hacker/the-flag`

flag: `pwn.college{w2gdJ-YqFUUlRTav-AB4ZnSw4Eq.QX3ATO0wyNwkzNyEzW}`

