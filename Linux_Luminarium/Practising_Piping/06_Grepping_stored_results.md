### Grepping stored results 

In preparation for more complex levels, we want you to:

1. Redirect the output of `/challenge/run` to `/tmp/data.txt`.
2. This will result in a hundred thousand lines of text, with one of them being the flag, in `/tmp/data.txt`.
3. Grep that for the flag!

**flag:** `pwn.college{Izent-6oQewWy7W2fN_vrggo_Ts.QX4EDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run > /tmp/data.txt`
`grep "pwn.college" /tmp/data.txt`

#### What I learnt: 
I learned to combine **output redirection** with `grep` to efficiently search for specific patterns in large datasets. This is a common and powerful workflow for analyzing log files or the output of noisy commands.


