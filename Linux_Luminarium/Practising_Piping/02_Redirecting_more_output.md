### Redirecting more output

Aside from redirecting the output of `echo`, you can, of course, redirect the output of any command. In this level, `/challenge/run` will once more give you a flag, but _only_ if you redirect its output to the file `myflag`. Your flag will, of course, end up in the `myflag` file!

**flag:**` pwn.college{Em_m3acj763eg0xueV0umpcexcG.QX1YTN0wyNwkzNyEzW}`

Command used: 
`/challenge/run > myflag`
`cat myflag`

First, I executed the `/challenge/run` binary using `>` operator to redirect its output to a file named `myflag`. By which the `stderr` text was printed to my terminal. Then I used the `cat` on `myflag`, which prompted me the flag.