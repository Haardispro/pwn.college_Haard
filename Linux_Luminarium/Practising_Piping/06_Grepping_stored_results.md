### Grepping stored results 

In preparation for more complex levels, we want you to:

1. Redirect the output of `/challenge/run` to `/tmp/data.txt`.
2. This will result in a hundred thousand lines of text, with one of them being the flag, in `/tmp/data.txt`.
3. Grep that for the flag!

Command used: 
`/challenge/run > /tmp/data.txt`
`grep "pwn.college" /tmp/data.txt`

flag: `pwn.college{Izent-6oQewWy7W2fN_vrggo_Ts.QX4EDO0wyNwkzNyEzW}`
