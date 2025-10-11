### Snooping on Configurations

Afterwards, Zardus can easily refer to the API key. In this level, users can use a valid API key to get the flag:

```
zardus@dojo:~$ flag_getter --key $FLAG_GETTER_API_KEY
Correct API key! Do you want me to print the key (y/n)? y
pwn.college{HACKED}
zardus@dojo:~$
```

Naturally, Zardus stores his key in `.bashrc`. Can you steal the key and get the flag?

**flag:** `pwn.college{sZH97VUtd8C9mXW5x7xI_CZniBo.0lM0EzNxwyNwkzNyEzW}`

Command used: 
- `cat /home/zardus/.bashrc`
- `flag_getter --key sk-4821690`

Zardus stores his key in `.bashrc` as usual, so I read it to get the key and subsequently get the flag.      



