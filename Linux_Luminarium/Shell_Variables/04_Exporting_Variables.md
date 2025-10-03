### Exporting Variables

In this challenge, you must invoke `/challenge/run` with the `PWN` variable exported and set to the value `COLLEGE`, and the `COLLEGE` variable set to the value `PWN` but _not_ exported (e.g., not inherited by `/challenge/run`). Good luck!

**flag:** `pwn.college{MweJYWjQxXfDwM0UqFEt72lk1Op.QXyYTN0wyNwkzNyEzW}`

Command used: 
`export PWN=COLLEGE`
`COLLEGE=PWN`
`/challenge/run PWN`

By default variables that are created are local to the shell session, after the session is closed the variables created are lost. Which means other commands can't make use of that stored variable. 

In this challenge, I exported the variable `PWN` which stored the value of `COLLEGE` . I set the `COLLEGE` value to `PWN` but not exported, so the command `/challenge/run` cannot use the variable, therefore after running `/challenge/run PWN` I got the flag. 