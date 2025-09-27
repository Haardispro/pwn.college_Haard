### Tab Completion 

This challenge has copied the flag into `/challenge/pwncollege`, and you can freely `cat` that file. But you can't type the filename: we used some serious trickery to make sure that you _must_ tab-complete it. Try it out!

flag: `pwn.college{MkU0bYg9ImyUkcFTIQU7PVz5XwB.0FN0EzNxwyNwkzNyEzW}`

Command used: `cat /challenge/pwn<tab>`

`<tab>` autocompletes incomplete command passed in the shell. On passing the above mentioned command and pressing tab, I got the flag. 
