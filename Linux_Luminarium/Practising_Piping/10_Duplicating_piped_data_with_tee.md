### Duplicating piped data with tee 

Now, you try it! This process' `/challenge/pwn` must be piped into `/challenge/college`, but you'll need to intercept the data to see what `pwn` needs from you!

Command used: 
`/challenge/pwn | tee arg_file | /challenge/college`
`/challenge/pwn --secret 0Xdh62f | /challenge/college`

flag: `pwn.college{0Xdh62afV6NYri9w0bJ8zYDE--f.QXxITO0wyNwkzNyEzW}`

