### Process Exit Codes 

In this challenge, you must retrieve the exit code returned by `/challenge/get-code` and then run `/challenge/submit-code` with that error code as an argument. Good luck!

**flag:** `pwn.college{E18yIX5D3ZGz6AePPB12B3QTGQN.QX5YDO1wyNwkzNyEzW}`

Command used: 
`/challenge/get-code`
`echo $?`
`/challenge/submit-code 71`

This is what I learnt: 
You can access the exit code of the most recently-terminated command using the special `?` variable (don't forget to prepend it with `$` to read its value!):

I found the code to be `71` and got the flag.

