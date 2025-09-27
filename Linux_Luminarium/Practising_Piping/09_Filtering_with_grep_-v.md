### Filtering with grep -v

Sometimes, the only way to filter to just the data you want is to filter _out_ the data you _don't_ want. In this challenge, `/challenge/run` will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word `DECOY` somehwere in the flag) mixed in with the real flag. You'll need to filter _out_ the decoys while keeping the real flag!

Command used: 
`/challenge/run | grep -v DECOY`

flag: `pwn.college{4cGJSAg0L8AXQFCXMkfLp_ja1Zk.0FOxEzNxwyNwkzNyEzW}`
