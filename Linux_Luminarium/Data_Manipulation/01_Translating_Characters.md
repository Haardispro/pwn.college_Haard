### Translating Characters

Now, you try it! In this level, `/challenge/run` will print the flag but will swap the casing of all characters (e.g., `A` will become `a` and vice-versa). Can you undo it with `tr` and get the flag?

**flag:** `pwn.college{wwmVTL4TJyi0Vs9fPPUA7p4Pm1C.01MxEzNxwyNwkzNyEzW}`

Command used: 
`/challenge/run | tr 'A-Za-z 'a-zA-Z' `

This is how the `tr` command works: 
`tr <before> <after>`

I had to lookup how to address all the letters from A to Z, I found out you can do that using `A-Za-z`. 

What my above mentioned command basically does is that, it switches all the instances of the letters A to Z in both cases(capital and small) to their opposite cases.

Basically,
`A-Z` -> `a-z`
`a-z` -> `A-Z` 