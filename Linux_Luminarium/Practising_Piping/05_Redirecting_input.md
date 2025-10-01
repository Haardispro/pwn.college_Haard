### Redirecting input

You can do interesting things with a lot of different programs using input redirection! In this level, we will practice using `/challenge/run`, which will require you to redirect the `PWN` file to it and have the `PWN` file contain the value `COLLEGE`! To write that value to the `PWN` file, recall the prior challenge on output redirection from `echo`!

Command used: 
`echo COLLEGE > PWN`

`/challenge/run < PWN`

The challenge was a two-step process. First, I created a file named `PWN` containing the word 'COLLEGE' using output redirection. Second, I used the input redirection operator (`<`) to feed the contents of the `PWN` file into the `/challenge/run` program, which then printed the flag.

#### What I learnt: 
I learned how to use the < operator to redirect a file's content as standard input (stdin) to a command. This is a powerful way to provide input to programs non-interactively.

