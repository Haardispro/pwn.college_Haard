### implicit relative path 


**Flag:** `pwn.college{wS2wm3ciq1f4W-nYUGlVC3N-QEU.QXxUTN0wyNwkzNyEzW}`

command used: 
`cd /challenge`
`./run`

Running `run` in the working directory won't return me the output of `/challenge/run` as it is a safety mechanism in Linux which prevents running of core utilities without providing the path. 
Therefore, running `./run` will run the program which is explicitly present in the current working directory. 
#### What I learnt? 
Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:

```console
hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ run
```

This will _not_ invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:

```
bash: run: command not found
```
