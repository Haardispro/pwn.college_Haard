### Exclusionary globbing 

Armed with this knowledge, go forth to `/challenge/files` and run `/challenge/run` with all files that don't start with `p`, `w`, or `n`!
**NOTE:** The `!` character has a different special meaning in bash when it's not the first character of a `[]` glob, so keep that in mind if things stop making sense! `^` does not have this problem, but is also not compatible with older shells.

**flag:** `pwn.college{AyV9b9rtyLE2FCtVnxaC3x5uqoS.QX2IDO0wyNwkzNyEzW}`

Command used:
`cd /challenge/files`
`/challenge/run [!pwn]*`

`!` basically excludes the files which start with the given first letters. 
I passed in the above mentioned commands to get the flag. 