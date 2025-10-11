### Level 0:
Challenge -> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

I opened up the man page for ssh and looked up how to open up specific ports. 
`man ssh`  is the command I used to view the manual for ssh. 

Command used: 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

### Level 0 -> Level 1
README:
```text
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
### Level 1 -> Level 2

Opening a dashed file in Linux
Looked up on google how to open up a dashed file on Linux. 
This is what the first result showed me. 
Using `-` as an argument refers to `dev/stdin` or `dev/stdout`
So, for this type of file I had to specify the full location of the file such as `./-` or use `<` operator in `cat`.  Running `cat ./-` will give me the same output

```bash
cat < - 
```

Password 
```text
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

### Level 2 -> Level 3

Spaces in the filename 

This problem involved in opening a file which had spaces in the file name. 
By using `\`  followed by a space after every space in the filename will give the desired output. The exact command used is mentioned below. 
Alternatively, you can also write your filename in quotation marks. 

Command used: 
```bash
cat spaces\ in\ this\ filename
cat "spaces in this filename"
```

Password
```text
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

### Level 3 -> Level 4

Challenge -> The password for the next level is stored in a hidden file in the **inhere** directory.

The bash command `la`  lists all the files in a given directory along with hidden ones. 
I looked up how to view hidden files in Linux, along with how to make hidden files in Linux and found this as a solution. 
Hidden files or directories are made by putting a period `.` before the file/directory name in Linux/Unix systems. 

Commands used:
```bash
cd inhere
ls -la #to list all files along with hidden ones 
cat ...Hiding-From-You
```

Password

```text
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

### Level 4 -> Level 5

Challenge -> The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

I used the knowledge from the dashed filename level to find out the answer here. But I am sure there's a better way to do it. I have to do something with the `file` command to find out which one is not executable and is a simple ascii text file. 

Commands used: 
```bash
cd inhere/
cat < -file00
cat < -file01
...... # until I found the file which contained ascii, which was -file07
```

Password

```text
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

### Level 5 -> Level 6

Command Used:
```bash
find ./maybehere0*/ -size 1033c
```

Password 
```text
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

### Level 6 -> Level 7

Command Used:
```bash
find / -user bandit7 -group bandit6 -size 33c
```

Password:
```text
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

### Level 7 -> Level 8

Command used:
```bash
grep "millionth" data.txt
```

Password:
```text
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

### Level 8 -> Level 9 

Command used: 
```bash
sort data.txt | uniq -u 
```

Password: 
```text
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

### Level 9 -> Level 10 

I found the password by just viewing the file using cat and looking for the only human readable string preceded by multiple "=". That was manual inspection method. So I have to lookup how to do it using a simple Linux command. 

Command used: 
```bash

```

Password:
```text
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

### Level 10 -> Level 11

Command used: 
```shell
cat data.txt | base64 --decode
base64 -d data.txt # didn't know this. 
```

Password: 
```text
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

### Level 11 -> Level 12

On searching for this cipher technique, I found out that its called ROT13. And on using the following command I got my password. 

Command used: 
```shell
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

Password:
```text
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

### Level 12 -> Level 13

data.txt was highly compressed using multiple compression utilities like bzip, gzip and tar. It took around 10-12 decompressions untill I reached ascii

Command used: 
```shell

```

Password:
```text
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```