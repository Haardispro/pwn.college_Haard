### Scripting with Multiple Conditions

For this challenge, write a script at `/home/hacker/solve.sh` that:

- Takes one argument
- If the argument is "hack", output "the planet"
- If the argument is "pwn", output "college"
- If the argument is "learn", output "linux"
- For any other input, output "unknown"

**flag:** `pwn.college{wfITgZRgw5dE6mduydGTuyrd7Tw.0FOzMDOxwyNwkzNyEzW}`

Contents of solve.sh: 
```bash
if [ "$1" == "hack" ]
then 
	echo "the planet"
elif [ "$1" == "pwn" ]
then
	echo "college"
elif [ "$1" == "learn" ]
then
	echo "linux"
else
	echo "unknown"
fi
```


