### Mixing globs 

Now, let's put the previous levels together! We put a few happy, but diversely-named files in `/challenge/files`. Go `cd` there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to `/challenge/run`) will match the files "challenging", "educational", and "pwning"!

**flag:** `pwn.college{gqlpXLgXO2LFwk_v4w6HurAwczD.QX1IDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run [pce]*`

In this challenge, I had to match the files "challenging", "educational" and "pwning" , by passing an argument which is 6 characters or less. 

From what I learnt from previous challenges, I can mix up globs, so this is how my command looked: 
- `/challenge/run [pce]*`

`[pce]` matches every file starting with letter `p`, `c` or `e`. 
`*` matches every character after the respective letters, which is `p`,`c` or `e`. 

There are only 3 files satisfy that condition, after passing the argument I got the flag.    