### Scripting with Conditionals

For this challenge, write a script at `/home/hacker/solve.sh` that:

- Takes one argument
- If the argument is "pwn", output "college"
- For any other input, output nothing

flag: `pwn.college{Mjw6x--tcEiqMVP4WexNEjgc3nu.0lNzMDOxwyNwkzNyEzW}`

This is what I created after I followed the instructions. Its basic if, else. I used basic programming logic to solve this.  
solve.sh
```bash
#!/bin/bash
if [ "$1" == "pwn"]
then 
	echo "college"
fi
```

