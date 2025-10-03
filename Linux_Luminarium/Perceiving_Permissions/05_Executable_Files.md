### Executable Files 

In this challenge, the `/challenge/run` program will give you the flag, but you must first make it executable! Remember your `chmod`, and get `/challenge/run` to tell you the flag!

**flag:** `pwn.college{MtyhPCOqTQaaMu6BjdIB2o8mS5t.QXyEjN0wyNwkzNyEzW}`

Command used: 
`chmod +x /challenge/run`
`/challenge/run`

`+x` argument makes the file executable, which means you can run a file using `./<filename>`. According to the challenge, I passed `+x` as an argument to `chmod` to make the file `/challenge/run` executable and then ran `/challenge/run` to get the flag.