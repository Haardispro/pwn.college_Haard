### Backgrounding Processes 

This level's `run` wants to see another copy of itself running, _not suspended_, and using the same terminal. How? Use the terminal to launch it, then suspend it, then _background_ it with `bg` and launch another copy while the first is running in the background!


**flag:** `pwn.college{YB4h6cCdB94JsYjbtGVQmlhqun6.QX3QDO0wyNwkzNyEzW}`

Command used: 
`/challenge/run`
`Ctrl-Z`
`bg`
`/challenge/run` 

`bg` command resumes a suspended program in the background, it basically does `/challenge/run &` . 
Followed the instructions and got the flag. 