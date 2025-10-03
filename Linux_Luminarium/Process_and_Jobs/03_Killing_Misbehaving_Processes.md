### Killing Misbehaving Processes

Your general workflow should be:

1. Check what processes are running.
2. Find `/challenge/decoy` in the list and figure out its process ID.
3. `kill` it.
4. Run `/challenge/run` to get the flag without being overwhelmed by decoys (you don't need to redirect its output; it'll write to the FIFO on its own).

Good luck!

Commands used:
1. `ps -ef`
```
 UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:02 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo
root           7       1  0 05:02 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 05:02 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 05:02 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 05:02 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     138  0 05:02 ?        00:00:00 sleep 6h
root         141     137  0 05:02 ?        00:00:00 sleep 6h
hacker       142     139  0 05:02 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  0 05:02 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --int
hacker       157     153  0 05:02 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       167     157  0 05:02 pts/0    00:00:00 ps -ef
```
2. `kill 142`
3. `/challenge/run &`
4. `cat /tmp/flag_fifo | tail -n 1`

**flag:** `pwn.college{8nZvbc6DCi92_Cd7zBG5zA6iwl3.0FNzMDOxwyNwkzNyEzW}`

Used my knowledge from previous challenges and modules to get the flag.



