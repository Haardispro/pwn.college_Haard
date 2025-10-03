### Multi-word Variables

Here, the shell reads `1337 SAUCE` as a single token, and happily sets that value to `VAR`. In this level, you'll need to set the variable `PWN` to `COLLEGE YEAH`. Good luck!

**flag:** `pwn.college{k4CZbQKDuzndPsYcEJJdI8I733a.QXwYTN0wyNwkzNyEzW}`

Command used: `PWN="COLLEGE YEAH"`

What I learnt is that you need to quote your value if it is a multi-word variable. I did just that and got the flag. 