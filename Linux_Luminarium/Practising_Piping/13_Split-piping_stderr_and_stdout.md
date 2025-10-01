### Split-piping stderr and stdout 

In this challenge, you have:

- `/challenge/hack`: this produces data on _stdout_ and _stderr_
- `/challenge/the`: you must redirect `hack`'s _stderr_ to this program
- `/challenge/planet`: you must redirect `hack`'s _stdout_ to this program

Go get the flag!

**flag:** `pwn.college{A2heJpeNj1vboK1kmEcYe3--0zH.QXxQDM2wyNwkzNyEzW}`

Command used: `/challenge/hack 2> >(/challenge/the) > >(/challenge/planet)`

To solve this, I split `/challenge/hack`'s output. then I used process substitution to create input streams for `/challenge/the` and `/challenge/planet`. Then I redirected **stderr** (`2>`) to one and **stdout** (`1>`) to the other in a single command.

#### What I learnt: 

I learned how to split **stdout** and **stderr** to different program inputs. The key is using **output process substitution** (`>(command)`) to create a writeable "file" for each destination program, then redirecting the specific file descriptors (`>` and `2>`) accordingly.

