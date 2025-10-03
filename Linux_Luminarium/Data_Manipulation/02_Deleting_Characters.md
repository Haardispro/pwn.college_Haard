### Deleting Characters 

Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: `^` and `%`) among the flag characters. Use `tr -d` to remove them!

**flag:** `pwn.college{ArYqkQifCE4vBrmABN0v4pEXjR3.0FNxEzNxwyNwkzNyEzW}`

Command used: 
`/challenge/run | tr -d %^`

The command `tr` can also be used to delete characters using the `-d` argument.

So I deleted the decoy characters `%` and `^` using the command mentioned above. 