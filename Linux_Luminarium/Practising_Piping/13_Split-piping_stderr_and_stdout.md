### Split-piping stderr and stdout 

In this challenge, you have:

- `/challenge/hack`: this produces data on _stdout_ and _stderr_
- `/challenge/the`: you must redirect `hack`'s _stderr_ to this program
- `/challenge/planet`: you must redirect `hack`'s _stdout_ to this program

Go get the flag!

Command used: `/challenge/hack 2> >(/challenge/the) > >(/challenge/planet)`
