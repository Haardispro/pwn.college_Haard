### Sorting Data

In this challenge, there's a file at `/challenge/flags.txt` containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end (we made sure of this when generating fake flags). Go get it!


**flag:** `pwn.college{oehM1AR1n_8ooliNMgu3-lqkes2.0FM0MDOxwyNwkzNyEzW}`

Command used: 
`sort /challenge/flags.txt`

The `sort` command sorts the text in a given text file in alphabetical order by default, but many other arguments can be passed to get different results. 

According to the challenge, I had to sort the flags in alphabetical order to get the flag. 
I used the above mentioned to get the flag on the last line of the sorted flags. 

#### Extra: 
You can make this command even better by using the `tail` command, which outputs only the last lines of a given output stream. 

`sort /challenge/flags.txt | tail -n 1`

This will directly get me the flag. 