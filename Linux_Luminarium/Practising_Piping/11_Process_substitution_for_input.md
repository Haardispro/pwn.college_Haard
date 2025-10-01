### Process substitution for input 

Now for your challenge! Recall what you learned in the `diff` challenge from [Comprehending Commands](https://pwn.college/linux-luminarium/commands). In that challenge, you diffed two files. Now, you'll diff two sets of command outputs: `/challenge/print_decoys`, which will print a bunch of decoy flags, and `/challenge/print_decoys_and_flag` which will print those same decoys plus the real flag.

Use process substitution with `diff` to compare the outputs of these two programs and find your flag!

**flag:** `pwn.college{UBAXiuf0WozDaZBvlS1XG4UTfqF.0lNwMDOxwyNwkzNyEzW}`

Command used: 
`diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)`

I needed to find the difference between two programs output. I used process substitution with `diff` to compare them without making files. `diff` showed the extra line, which was the flag.

#### What I learnt: 
I learnt about process substitution `<(command)`. Its a way to use a command output like a file. This is useful for commands like `diff` that need file inputs. 



