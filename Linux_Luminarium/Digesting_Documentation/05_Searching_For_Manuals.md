### Searching For Manuals

This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the man pages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right man page, read the `man` page manpage by doing: `man man`!

flag: `pwn.college{8CGiiBfPK53wKUp_4d1wgU3k2MX.QX2EDO0wyNwkzNyEzW}`

Commands used: 
`man -k challenge`
`man iifwpdwgkw`
`/challenge/challenge --iifwpd 853`

By looking at the manual page for the `man` command, I found out that, you can search for manual entry keywords by passing `-k` argument followed by the keyword. 
That means, whichever manual entry contains that keyword will be shown. 

I used that knowledge to find out which manual entry contains the keyword. 

Looking at the man page for `iifwpdwgkw` , I saw what was needed to get the flag and I got the flag accordingly. 