### An Epic Filesystem Quest

In this challenge, I have _hidden the flag_! Here, you will use `ls` and `cat` to follow my breadcrumbs and find it! Here's how it'll work:

0. Your first clue is in `/`. Head on over there.
1. Look around with `ls`. There'll be a file named HINT or CLUE or something along those lines!
2. `cat` that file to read the clue!
3. Depending on what the clue says, head on over to the next directory (or don't!).
4. Follow the clues to the flag!

Good luck!

**Flag:** `pwn.college{UV4dbtuk7Y5TXPHMOOWh1aLGKE1.QX5IDO0wyNwkzNyEzW}`

This is what I did: 

```bash  
> cd /
> ls 
MESSAGE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var      bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
> cat MESSAGE
"Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/pip/_vendor/cachecontrol/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'."
> cd /usr/local/lib/python3.8/dist-packages/pip/_vendor/cachecontrol/__pycache__
> ls -a
.   .CUE                     _cmd.cpython-38.pyc     cache.cpython-38.pyc      filewrapper.cpython-38.pyc  serialize.cpython-38.pyc
..  __init__.cpython-38.pyc  adapter.cpython-38.pyc  controller.cpython-38.pyc  heuristics.cpython-38.pyc   wrapper.cpython-38.pyc
> cat .CUE 
"Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/snip-lib/racket

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'."
> cd /usr/share/racket/pkgs/snip-lib/racket
> ls -a 
.  ..  .BRIEF  compiled  snip  snip.rkt
> cat .BRIEF
"Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/arch/csky

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!"
> ls /opt/linux/linux-5.4/arch/csky
Kconfig  Kconfig.debug  Makefile  WHISPER-TRAPPED  abiv1  abiv2  boot  configs  include  kernel  lib  mm
> cat /opt/linux/linux-5.4/arch/csky/WHISPER-TRAPPED
"Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/arch/mips/include/asm/mach-ar7

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!"
> ls /opt/linux/linux-5.4/arch/mips/include/asm/mach-ar7
README-TRAPPED  ar7.h  irq.h  prom.h  spaces.h
> cat /opt/linux/linux-5.4/arch/mips/include/asm/mach-ar7/README-TRAPPED
"Yahaha, you found me!
The next clue is in: /usr/share/doc/libtk8.6

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'."
> cd /usr/share/doc/libtk8.6
> ls 
CLUE  changelog.Debian.gz  copyright
> cat CLUE 
"Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/clk_mgr/dce112

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'."
> cd /opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/clk_mgr/dce112
> ls -a 
.  ..  .SNIPPET  dce112_clk_mgr.c  dce112_clk_mgr.h
> cat .SNIPPET 
"Great sleuthing!
The next clue is in: /usr/share/racket/pkgs/redex-benchmark/redex/benchmark/models/let-poly/compiled"
> cd /usr/share/racket/pkgs/redex-benchmark/redex/benchmark/models/let-poly/compiled
> ls 
TIP                 let-poly-1_rkt.zo   let-poly-3_rkt.zo   let-poly-5_rkt.zo   let-poly-7_rkt.zo      typed-info_rkt.zo
generators_rkt.dep  let-poly-2_rkt.dep  let-poly-4_rkt.dep  let-poly-6_rkt.dep  let-poly-info_rkt.dep  util_rkt.dep
generators_rkt.zo   let-poly-2_rkt.zo   let-poly-4_rkt.zo   let-poly-6_rkt.zo   let-poly-info_rkt.zo   util_rkt.zo
let-poly-1_rkt.dep  let-poly-3_rkt.dep  let-poly-5_rkt.dep  let-poly-7_rkt.dep  typed-info_rkt.dep
> cat TIP 
"Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/redex-benchmark/redex/benchmark/models/poly-stlc/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'."
> cd /usr/share/racket/pkgs/redex-benchmark/redex/benchmark/models/poly-stlc/compiled
> ls 
SECRET               poly-stlc-2_rkt.dep  poly-stlc-4_rkt.zo   poly-stlc-7_rkt.dep  poly-stlc-9_rkt.zo      util_rkt.dep
generators_rkt.dep   poly-stlc-2_rkt.zo   poly-stlc-5_rkt.dep  poly-stlc-7_rkt.zo   poly-stlc-info_rkt.dep  util_rkt.zo
generators_rkt.zo    poly-stlc-3_rkt.dep  poly-stlc-5_rkt.zo   poly-stlc-8_rkt.dep  poly-stlc-info_rkt.zo
poly-stlc-1_rkt.dep  poly-stlc-3_rkt.zo   poly-stlc-6_rkt.dep  poly-stlc-8_rkt.zo   typed-info_rkt.dep
poly-stlc-1_rkt.zo   poly-stlc-4_rkt.dep  poly-stlc-6_rkt.zo   poly-stlc-9_rkt.dep  typed-info_rkt.zo
> cat SECRET 
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{UV4dbtuk7Y5TXPHMOOWh1aLGKE1.QX5IDO0wyNwkzNyEzW}
```

Long aah quest. 