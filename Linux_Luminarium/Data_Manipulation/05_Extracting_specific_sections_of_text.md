### Extracting specific sections of text 

In this challenge, the `/challenge/run` program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns. Use `cut` to extract the flag characters, then pipe them to `tr -d "\n"` (like the previous level!) to join them together into a single line. Your solution will look something like `/challenge/run | cut ??? | tr ???`, with the `???` filled out.

**flag:** `pwn.college{QGZ3wf8Pr-F-KZl1edeOjVAUC9C.01NxEzNxwyNwkzNyEzW}`

Commands used: 
`/challenge/run | cut -d " " -f 2 | tr -d "\n"`

This is what `/challenge/run` gave me: 

```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
9435 p
25990 w
20563 n
6139 .
1805 c
32070 o
1719 l
24626 l
7340 e
27170 g
4846 e
23881 {
4972 Q
17452 G
25122 Z
21436 3
..
..
..
```


So what I know is that, the flag is on the second column and is separated by an empty space.

so, the cut command would look something like this: 
`cut -d " " -f 2`

Every character is on a new line, so I have to remove the newline character as well using the `tr` command. So, the `tr` command would look something like this: 
`tr -d "\n"`

Combining all of that together using pipes, I got the flag using the above mentioned command. 