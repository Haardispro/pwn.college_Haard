### Scripting with Default Cases 

For this challenge, write a script at `/home/hacker/solve.sh` that:

- Takes one argument
- If the argument is "pwn", output "college"
- For any other input, output "nope"

**flag:** `pwn.college{g4R50nBfyD-rJWBMsQ4HbmT3gYA.01NzMDOxwyNwkzNyEzW}`

solve.sh
```bash
if [ "$1" == "pwn" ]
then 
	echo "college"
else
	echo "nope"
fi
```

Used basic programming logic to create the script, got the flag after following the instructions. 