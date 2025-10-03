### Sniffing Input 

Your mission is to use your continued write access to Zardus's `.bashrc` to intercept this flag. Remember how you hijacked commands in the [Pondering PATH](https://pwn.college/linux-luminarium/path) module? Can you use that capability to hijack the `flag_checker`?


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
