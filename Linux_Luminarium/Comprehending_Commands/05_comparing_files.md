### comparing files 

Now for your challenge! There are two files in `/challenge`:

- `/challenge/decoys_only.txt` contains 100 fake flags
- `/challenge/decoys_and_real.txt` contains all 100 fake flags plus the one real flag

Use `diff` to find what's different between these files and get your flag!


**Flag:** `pwn.college{wfQuhx_K7hV1_L_qHPwxLGrNisH.01MwMDOxwyNwkzNyEzW}`


Command used: `diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt`

The `diff` command finds the difference between two files. It works something like this: 
- `diff <file1> <file2>`
That is what I did and obtained the flag. 