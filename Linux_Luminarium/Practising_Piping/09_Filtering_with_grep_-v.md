### Filtering with grep -v

Sometimes, the only way to filter to just the data you want is to filter _out_ the data you _don't_ want. In this challenge, `/challenge/run` will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word `DECOY` somehwere in the flag) mixed in with the real flag. You'll need to filter _out_ the decoys while keeping the real flag!

**flag:** `pwn.college{4cGJSAg0L8AXQFCXMkfLp_ja1Zk.0FOxEzNxwyNwkzNyEzW}`

Command used: 
`/challenge/run | grep -v DECOY`

The program's output contained many decoy flags marked with the word "DECOY". I piped the output to `grep -v "DECOY"` to invert the search and display only the line that did not contain the decoy keyword, revealing the true flag.

## What I Learned

I learned about the **`-v`** option for `grep`, which inverts the match. It's a useful tool for filtering out noise or unwanted data to isolate the specific information you need.

