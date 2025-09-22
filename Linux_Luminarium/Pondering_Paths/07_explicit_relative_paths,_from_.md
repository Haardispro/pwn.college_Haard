### explicit relative paths, from /

Of course, if your current working directory is `/`, the above relative paths are equivalent to the above absolute paths.

---
**Flag:** `pwn.college{QhS4qzh2IxHqQqyMCLLhWQhvuh7.QXwUTN0wyNwkzNyEzW}`

command used: 
`cd /`
`./challenge/run`

Changed to the root directory and ran `./challenge/run` the `./` selects the current working directory. That gave me the flag. 