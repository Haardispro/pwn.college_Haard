### Grepping live output

Now try it for yourself! `/challenge/run` will output a hundred thousand lines of text, including the flag. Grep for the flag!

**flag:** `pwn.college{YWviX52d-6-qRO9zzQKc2UymGAK.QX5EDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run | grep pwn.college`

Instead of saving the output to a file first, I piped the standard output of `/challenge/run` directly into the standard input of `grep`. This allowed me to search for the flag pattern `pwn.college{`

