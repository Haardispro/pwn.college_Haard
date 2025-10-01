### Appending output

To practice, run `/challenge/run` with an append-mode redirect of the output to the file `/home/hacker/the-flag`. The practice will write the first half of the flag to the file, and the second half to `stdout` if `stdout` is redirected to the file. If you properly redirect in append-mode, the second half will be appended to the first, but if you redirect in _truncation_ mode (`>`), the second half will _overwrite_ the first and you won't get the flag!

**flag:** `pwn.college{w2gdJ-YqFUUlRTav-AB4ZnSw4Eq.QX3ATO0wyNwkzNyEzW}`

Command used: 
`/challenge/run >> /home/hacker/the-flag`

The program wrote the flag in two parts. To prevent the second part from overwriting the first, I redirected the program's output using the append operator (`>>`) into the file `the-flag`. Then I read the file to get the complete flag.

```
hacker@piping~appending-output:~$ /challenge/run >> the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!

hacker@piping~appending-output:~$ /challenge/run >> the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
...
hacker@piping~appending-output:~$ cat the-flag
 |
\|/ This is the first half:
 v
pwn.college{w2gdJ-YqFUUlRTav-AB4ZnSw4Eq.QX3ATO0wyNwkzNyEzW}
                              ^
     that is the second half /|\
                              |

```

