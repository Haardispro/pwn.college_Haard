### Deleting Newlines

Now, let's combine this with deletion. In this challenge, we'll inject a bunch of newlines into the flag. Delete them with `tr`'s `-d` flag and the _escaped_ newline specification!

**flag:** `pwn.college{QSw0W9gQavZZBDmEIer4gQ0ivww.0VNxEzNxwyNwkzNyEzW}`

Command used: 
`/challenge/run | tr -d "\n" `

Using the knowledge of the previous challenge, I deleted the all the newline characters by using the `-d` argument of the `tr` command. 