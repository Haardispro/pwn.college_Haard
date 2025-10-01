### Writing to multiple programs

Now it's your turn! In this challenge, we have `/challenge/hack`, `/challenge/the`, and `/challenge/planet`. Run the `/challenge/hack` command, and duplicate its output as input to both the `/challenge/the` and the `/challenge/planet` commands!

**flag:** `pwn.college{MDXODHO_l0mhoh2S0Og6stS8blk.QXwgDN1wyNwkzNyEzW}`

Command used: 
`/challenge/hack | tee>(/challenge/the) | /challenge/planet`

I had to send the output of `/challenge/hack` to two other programs. I piped the output to `tee`, and then used output process substitution `>(command)` for both `/challenge/the` and `/challenge/planet`. This made them look like files to `tee`, so it send the data to both.

#### What I learnt: 
I learned how to use **output process substitution** `>(command)` to make a program's input look like a file. You can use it with `tee` to send one output to many command's inputs at once. Its a cool trick.

