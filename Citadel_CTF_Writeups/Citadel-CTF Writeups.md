
# The Ripper 

### Description 

The guardian of this floor steps from the shadows. Known only as Jack the Ripper, he watches you carefully. He proclaims himself merciful and hands you a word list to help. He asks you to find the passcode hidden in this hash `$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa`. The word list is your only aid. Only by combining the two correctly can you uncover the key and move on to the next floor. Flag format: `citadel{password}`
### Solve: 

Two files, namely `hash.txt` and `wordlist.txt` were given.   
`hash.txt` : 
```
$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa
```
`wordlist.txt`: 
```
flag_Fake_Fl@G_4_Ph4K3_P|4Y3Rs2025
0xFake_fla9_4_f4k3_p14y3r52025
flag_FAKE_FL4G_4_F@K3_P|4Y3R5
flag_fake_fla9_4_phake_pl4y3r$!
flag_fake_flag_4_fak3_p14y3rs2025
the_fake_fl@9_4_phake_p|4y3r$!
real_fake_flag_4_f@ke_p14y3r5!!
real_Fake_fl@g_4_f4ke_pl4y3r5!
the_fake_fl@9_4_f4ke_p14y3rs2025
the_FAKE_FLA9_4_F4K3_PL4Y3R52025
...
..
.
```

What I know that John The Ripper is a hash cracking utility that I can use to crack a hash as the one provided above.

Using the provided wordlist, I managed to crack the hash. 

```bash
> john --wordlist=wordlist.txt hash.txt
Loaded 1 password hash (bcrypt [Blowfish 32/64 X3])
No password hashes left to crack (see FAQ)
> john --show hash.txt
?:fake_flag_4_fake_pl4y3rs

1 password hash cracked, 0 left
```

Final flag: `citadel{fake_flag_4_fake_pl4y3rs}`

---
# BRATCHA 

### Description 

A clear chime rolls through the chamber and a new crest ignites on your badge – a quiet promotion. The outer ring is behind you. From here, the Citadel opens its inner systems, and the locks grow heavier because the keys are worth more. Your answers now carry more weight – and earn more in return. The citadel welcomes you to the inner climb.

Near the gate to the next floor you come across a CAPTCHA verification test, but it has been covered by scratches on the decaying wall and misleading letters stopping you from finding the correct key, all to prove you’re human.

### Solve: 
![[Pasted image 20251010213716.jpg]]

The following image was provided in order to unlock a pastebin link which contained the flag.
What we can clearly observe is the overlapped letters: `c/s g/q x/y h/n x/v B/D h/n S/Z`

Eventually a python script was made to try out all the combinations of the link. 
```python 
import requests
import itertools

positions = [
    ['s','c'],
    ['g','q'],
    ['x','y'],
    ['h','n'],
    ['x','v'],
    ['B','D'],
    ['h','n'],
    ['Z','S']
]

combinations = [''.join(p) for p in itertools.product(*positions)]

url_template = "https://pastebin.com/{}"

for code in combinations:
    url = url_template.format(code)
    try:
        response = requests.get(url, timeout=5)
        if response.status_code != 404:
            print(f"[FOUND] {url} (Status code: {response.status_code})")
        else:
            print(f"[NOT FOUND] {url}")
    except requests.RequestException as e:
        print(f"[ERROR] {url} ({e})")

```

What this script does is, it sends a GET request to every pastebin link, if it returns 404, then that link is invalid. 

This program kept running, and we stopped the program when we got the valid link. 
```
...
[NOT FOUND] https://pastebin.com/sqxhvDnZ
[NOT FOUND] https://pastebin.com/sqxhvDnS
[FOUND] https://pastebin.com/sqxnxBhZ (Status code: 200)
[NOT FOUND] https://pastebin.com/sqxnxBhS
[NOT FOUND] https://pastebin.com/sqxnxBnZ
...
```

I found the correct link, and it led me to the following text, which contained the flag. 

```
Congrats!

You've proven you're human.

Here's your flag:

citadel{1m_3v3rywh3r3_1m_s0_jul1a}
```

