### Alias 

alias flag_checker="bash /home/hacker/flag_checker"

```

`/home/hacker/flag_checker`:
```bash
echo -n "Type the flag, victim: "
read -r candidate
echo "\n$candidate"
echo 
if [ "$candidate" = "$(cat /flag)" ]; then
	echo "Correct!"
	# putting echo here would cause an error and won't show the flag as the hacker user doesn't have read permissions to /flag, better to just get the input flag after read
	exit 0
else
	echo "Incorrect!"
	exit 1
fi
```


flag: `pwn.college{YJtNDzuqXSN5OODAZvsUFogdJMS.0VNzEzNxwyNwkzNyEzW}`
