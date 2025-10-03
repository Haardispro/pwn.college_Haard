### Cracking passwords

If a hacker gets their hands on a leaked `/etc/shadow`, they can start cracking passwords and wreaking havoc. The cracking can be done via the famous [John the Ripper](https://www.openwall.com/john/), as so:

```console
hacker@dojo:~$ john ./my-leaked-shadow-file
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Will run 32 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
password1337      (zardus)
1g 0:00:00:22 3/3 0.04528g/s 10509p/s 10509c/s 10509C/s lykys..lank
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@dojo:~$
```

Here, John the Ripper cracked Zardus' leaked password hash to find the real value of `password1337`. Poor Zardus!

This level simulates this story, giving you a leak of `/etc/shadow` (in `/challenge/shadow-leak`). Crack it (this could take a few minutes), `su` to `zardus`, and run `/challenge/run` to get the flag!

**flag:** `pwn.college{w6bohWtUKGA84nKbLzafkaIDC9O.QX3UDN1wyNwkzNyEzW}`

Commands used: 
`john /challenge/shadow-leak`
`su zardus`
`/challenge/run`

Passwords of different users and the root is stored in a file `/etc/shadow`. All these passwords are stored in the form of hashes and are not in human readable form. 

John The Ripper tries to crack these hashes and get the password. 

I used John the ripper to crack the password of the zardus user and changed my user to zardus to get the flag.  