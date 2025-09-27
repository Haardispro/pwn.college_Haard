### Matching with []

Try it here! We've placed a bunch of files in `/challenge/files`. Change your working directory to `/challenge/files` and run `/challenge/run` with a single argument that bracket-globs into `file_b`, `file_a`, `file_s`, and `file_h`!

**flag:** `pwn.college{sWUeqftHjA1Bvk0crR0WXRjOST4.QXzIDO0wyNwkzNyEzW}`

Command used: 
`cd /challenge/files`
`/challenge/run file_[absh]`

I changed my directory to `/challenge/files` as per mentioned in the challenge. My job was to bracket-glob `file_a`, `file_b`, `file_c` and `file_h` and I did just that using the command `/challenge/run file_[bash]`. 

#### What I learnt: 
The square brackets are, essentially, a limited form of `?`, in that instead of matching any character, `[]` is a wildcard for some subset of potential characters, specified within the brackets. For example, `[pwn]` will match the character `p`, `w`, or `n`.

