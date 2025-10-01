### Redirecting errors 

Let's put this into practice! In this challenge, you will need to redirect the output of `/challenge/run`, like before, to `myflag`, and the "errors" (in our case, the instructions) to `instructions`. You'll notice that nothing will be printed to the terminal, because you have redirected everything! You can find the instructions/feedback in `instructions` and the flag in `myflag` when you successfully pull this off!

**flag:** ` pwn.college{w-O3S3KGHoUlilCm5Po8m1L5I8W.QX3YTN0wyNwkzNyEzW}`

Command used: 
`/challenge/run > myflag 2> instructions`

`cat myflag`

The task was to save the program's normal output and its error messages into separate files. I redirected standard output (FD 1) to `myflag` and standard error (FD 2) to `instructions`. After running the command, the flag was found in the `myflag` file.

