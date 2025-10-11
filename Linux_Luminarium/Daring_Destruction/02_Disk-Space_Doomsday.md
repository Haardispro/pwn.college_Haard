### Disk-Space Doomsday 

This challenge forces you to fill the disk and then clean up. The process:

1. Fill your disk.
2. Run `/challenge/check`. It will attempt to create a 1 megabyte temporary file. If that fails, you pass the first stage and the checker will ask you to free the space.
3. Delete the file you made (with `rm`) to clear up the space.
4. Run `/challenge/check` a second time. If it can now create the temporary file (i.e., you successfully cleaned up your home directory), you’ll receive the flag.


**flag:** `pwn.college{QjxVGMeu80hmT4E9eC5wqqFRRT-.0lMyEzNxwyNwkzNyEzW}`

Commands I used: 
1. `touch big_file.txt` -> Made a file that will contain a lot of data
2. `yes > big_file.txt` -> piped output of yes to the big file 
3. `/challenge/check` -> this checks if the disk space is clogged up or not, then asks to clean up disk space 
4. `rm big_file.txt` -> Cleaned up disk 
5. `/challenge/check` -> Checks if the big file is removed, then it spits out the flag. 

