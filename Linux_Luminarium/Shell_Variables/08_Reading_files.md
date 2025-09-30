### Reading files 

What happened there? The example redirects `some_file` into the _standard input_ of `read`, and so when `read` reads into `VAR`, it reads from the file! Now, use that to read `/challenge/read_me` into the `PWN` environment variable, and we'll give you the flag! The `/challenge/read_me` will keep changing, so you'll need to read it right into the `PWN` variable with one command!

Command used: 
`read PWN < /challenge/read_me`

flag: `pwn.college{oQXHL4kXn_YGjt5p1AAzcIqtfzG.QXwIDO0wyNwkzNyEzW}`

