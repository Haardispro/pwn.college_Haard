### Process substitution for input 

Now for your challenge! Recall what you learned in the `diff` challenge from [Comprehending Commands](https://pwn.college/linux-luminarium/commands). In that challenge, you diffed two files. Now, you'll diff two sets of command outputs: `/challenge/print_decoys`, which will print a bunch of decoy flags, and `/challenge/print_decoys_and_flag` which will print those same decoys plus the real flag.

Use process substitution with `diff` to compare the outputs of these two programs and find your flag!

Command used: 
`diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)`

flag: `pwn.college{UBAXiuf0WozDaZBvlS1XG4UTfqF.0lNwMDOxwyNwkzNyEzW}`
