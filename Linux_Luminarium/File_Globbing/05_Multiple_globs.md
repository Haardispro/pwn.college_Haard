### Multiple globs

Now you try it. We put a few happy, but diversely-named files in `/challenge/files`. Go `cd` there and run `/challenge/run`, providing a single argument: a short (3 characters or less) globbed word with two `*` globs in it that covers every word that contains the letter `p`.

**flag:** `pwn.college{4iD7-ebp6IT5mILt7Wm9oXwP3oK.0lM3kjNxwyNwkzNyEzW}`

Command used: 
`cd /challenge/files`
`/challenge/run *p*`

According the challenge, I had to match every file that contains the letter `p`. 
`*p` matches every file which contain any character before the letter `p`. `p*` matches every character after the letter `p`. Combining both we get `*p*`, which matches every character before and after the letter `p`. 