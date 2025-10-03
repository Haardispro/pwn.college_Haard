### Reading files 

What happened there? The example redirects `some_file` into the _standard input_ of `read`, and so when `read` reads into `VAR`, it reads from the file! Now, use that to read `/challenge/read_me` into the `PWN` environment variable, and we'll give you the flag! The `/challenge/read_me` will keep changing, so you'll need to read it right into the `PWN` variable with one command!

**flag:** `pwn.college{oQXHL4kXn_YGjt5p1AAzcIqtfzG.QXwIDO0wyNwkzNyEzW}`

Command used: 
`read PWN < /challenge/read_me`

By using my knowledge from Practising piping, I took the value of `/challenge/read_me` as an input to the `read` command, that resulted in me getting the flag.

#### What I learnt: 

You can read files and store it in a variable using the `read` command 