### Learning Complex Usage 

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!


flag: `pwn.college{0pDVcnzhIQ1QX7k_syChms-Q-ia.QX1ITO0wyNwkzNyEzW}`

Command used: 
`/challenge/challenge --printfile /flag`

According to the documentation for `/challenge/challenge`, this program allows me to print the contents of the file to the terminal when the `--printfile` argument is passed. 

The `--printfile` should be followed by the absolute file path. 

I put that into practice and got the flag. 