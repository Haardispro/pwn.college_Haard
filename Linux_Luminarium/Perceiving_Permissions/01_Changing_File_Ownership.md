### Changing File Ownership 

In this level, we will practice changing the owner of the `/flag` file to the `hacker` user, and then read the flag. For this challenge only, I made it so that you can use chown to your heart's content as the `hacker` user (again, typically, this requires you to be `root`). Use this power wisely and chown away!


**flag:** `pwn.college{cPIcNd6c1p3Zt5zJLSWUiyjKz3l.QXxEjN0wyNwkzNyEzW}`

Command used: 
`chown hacker /flag`
`cat /flag`

We can change the ownership of a file using the `chown` command. It works something like this: 
`chown [username] [file]`

I did just that and read `/flag` using the `cat` command. 



