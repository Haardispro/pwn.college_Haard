### Redirecting output

In this challenge, you must use this input redirection to write the word `PWN` (all uppercase) to the filename `COLLEGE` (all uppercase).

**flag:** `pwn.college{kS4iVDX_k3I9n6h7LU6Qesoe9kB.QX0YTN0wyNwkzNyEzW}`

Command used: `echo PWN > COLLEGE`

The `>` operator redirects all the output of one function to a given file passed as an argument. 
According to the challenge, I had to write the word `PWN` to the filename `COLLEGE`. I did that using the `echo` command which prints whatever is passed as an argument and redirected the output of `echo` to the filename `COLLEGE`.