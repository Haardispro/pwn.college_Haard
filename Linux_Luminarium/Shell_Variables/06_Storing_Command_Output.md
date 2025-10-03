### Storing Command Output

Neat! Now, you practice. Read the output of the `/challenge/run` command directly into a variable called `PWN`, and it will contain the flag!

**flag:** `pwn.college{IUt3I7viJoRjJKGtbzBii4ovNk6.QX1cDN1wyNwkzNyEzW}`

Command used: 
`PWN=$(/challenge/run)`
`echo $PWN`


The challenge asked me to store the value of the command `/challenge/run` to the value `PWN`. I did that using the above mentioned command and then using `echo` to print out the value of the variable `PWN`.

#### What I learnt : 

We can use something called  **Command Substitution** to store the value of a command to a given variable. 
`VAR = $(command)`

