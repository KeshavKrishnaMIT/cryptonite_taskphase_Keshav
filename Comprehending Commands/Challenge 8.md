# An epic filesystem quest

```bash
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
NOTE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat NOTE
Yahaha, you found me!
The next clue is in: /usr/lib/python3/dist-packages/numpy/linalg/__pycache__

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ ls  /usr/lib/python3/dist-packages/numpy/linalg/__pycache__
README  __init__.cpython-38.pyc  info.cpython-38.pyc  linalg.cpython-38.pyc  setup.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/$ ls README
ls: cannot access 'README': No such file or directory
hacker@commands~an-epic-filesystem-quest:/$ cat README
cat: README: No such file or directory
hacker@commands~an-epic-filesystem-quest:/$ ls-a README
ssh-entrypoint: ls-a: command not found
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/python3/dist-packages/numpy/linalg/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/numpy/linalg/__pycache__$ ls
README  __init__.cpython-38.pyc  info.cpython-38.pyc  linalg.cpython-38.pyc  setup.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/numpy/linalg/__pycache__$ ls -a README
README
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/numpy/linalg/__pycache__$ cat README
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/at-exp-lib

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/numpy/linalg/__pycache__$ cd  /usr/share/racket/pkgs/at-exp-lib
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/at-exp-lib$ ls
LICENSE.txt  SNIPPET  at-exp  info.rkt  scribble
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/at-exp-lib$ cat SNIPPET
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/elftools/elf/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/at-exp-lib$ cd /usr/local/lib/python3.8/dist-packages/elftools/elf/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/elftools/elf/__pycache__$ ls
REVELATION                descriptions.cpython-38.pyc  enums.cpython-38.pyc        notes.cpython-38.pyc       segments.cpython-38.pyc
__init__.cpython-38.pyc   dynamic.cpython-38.pyc       gnuversions.cpython-38.pyc  relocation.cpython-38.pyc  structs.cpython-38.pyc
constants.cpython-38.pyc  elffile.cpython-38.pyc       hash.cpython-38.pyc         sections.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/elftools/elf/__pycache__$ cat REVELATION
Great sleuthing!
The next clue is in: /usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/elftools/elf/__pycache__$ cd /usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ ls -a
.  ..  .TIP  ld  ld64
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat .TIP
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/gui-lib/embedded-gui/private/compiled

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ ls
ld  ld64
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ ls -a
.  ..  .TIP  ld  ld64
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat .TIP
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/gui-lib/embedded-gui/private/compiled

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ ls -a ls -a /usr/share/racket/pkgs/gui-lib/embedded-gui/private/compiled
ls: cannot access 'ls': No such file or directory
/usr/share/racket/pkgs/gui-lib/embedded-gui/private/compiled:
.                           dllist_rkt.dep                  lines_rkt.zo                       snip-lib_rkt.dep
..                          dllist_rkt.zo                   locked-pasteboard_rkt.dep          snip-lib_rkt.zo
NUGGET-TRAPPED              embedded-message_rkt.dep        locked-pasteboard_rkt.zo           snip-wrapper_rkt.dep
aligned-pasteboard_rkt.dep  embedded-message_rkt.zo         on-show-editor_rkt.dep             snip-wrapper_rkt.zo
aligned-pasteboard_rkt.zo   fixed-width-label-snip_rkt.dep  on-show-editor_rkt.zo              stretchable-editor-snip_rkt.dep
alignment-helpers_rkt.dep   fixed-width-label-snip_rkt.zo   on-show-pasteboard_rkt.dep         stretchable-editor-snip_rkt.zo
alignment-helpers_rkt.zo    grey-editor_rkt.dep             on-show-pasteboard_rkt.zo          suppress-modify-editor_rkt.dep
alignment_rkt.dep           grey-editor_rkt.zo              program-editor_rkt.dep             suppress-modify-editor_rkt.zo
alignment_rkt.zo            grid-alignment_rkt.dep          program-editor_rkt.zo              tabbable-text_rkt.dep
button-snip_rkt.dep         grid-alignment_rkt.zo           really-resized-pasteboard_rkt.dep  tabbable-text_rkt.zo
button-snip_rkt.zo          interface_rkt.dep               really-resized-pasteboard_rkt.zo   verthoriz-alignment_rkt.dep
cue-text_rkt.dep            interface_rkt.zo                single-line-text_rkt.dep           verthoriz-alignment_rkt.zo
cue-text_rkt.zo             lines_rkt.dep                   single-line-text_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat NUGGET-TRAPPED
cat: NUGGET-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat /usr/share/racket/pkgs/gui-lib/embedded-gui/private/compiled/NUGGET-TRAPPED
Lucky listing!
The next clue is in: /opt/aflplusplus/qemu_mode/qemuafl/hw/ppc

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ ls -a /opt/aflplusplus/qemu_mode/qemuafl/hw/ppc
.                 fw_cfg.c        pnv_bmc.c    ppc405.h         ppc_booke.c       spapr_drc.c     spapr_pci_nvlink2.c  trace.h
..                mac.h           pnv_core.c   ppc405_boards.c  ppce500_spin.c    spapr_events.c  spapr_pci_vfio.c     virtex_ml507.c
EVIDENCE-TRAPPED  mac_newworld.c  pnv_homer.c  ppc405_uc.c      prep.c            spapr_hcall.c   spapr_rng.c
Kconfig           mac_oldworld.c  pnv_lpc.c    ppc440.h         prep_systemio.c   spapr_iommu.c   spapr_rtas.c
e500-ccsr.h       meson.build     pnv_occ.c    ppc440_bamboo.c  rs6000_mc.c       spapr_irq.c     spapr_rtas_ddw.c
e500.c            mpc8544_guts.c  pnv_pnor.c   ppc440_pcix.c    sam460ex.c        spapr_numa.c    spapr_rtc.c
e500.h            mpc8544ds.c     pnv_psi.c    ppc440_uc.c      spapr.c           spapr_nvdimm.c  spapr_tpm_proxy.c
e500plat.c        pef.c           pnv_xscom.c  ppc4xx_devs.c    spapr_caps.c      spapr_ovec.c    spapr_vio.c
fdt.c             pnv.c           ppc.c        ppc4xx_pci.c     spapr_cpu_core.c  spapr_pci.c     trace-events
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat /opt/aflplusplus/qemu_mode/qemuafl/hw/ppc
cat: /opt/aflplusplus/qemu_mode/qemuafl/hw/ppc: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat EVIDENCE-TRAPPED
cat: EVIDENCE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cat /opt/aflplusplus/qemu_mode/qemuafl/hw/ppc/EVIDENCE-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/drracket/repo-time-stamp

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/rustlib/x86_64-unknown-linux-gnu/bin/gcc-ld$ cd  /usr/share/racket/pkgs/drracket/repo-time-stamp
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/drracket/repo-time-stamp$ ls -a
.  ..  ALERT  compiled  doc.txt  info.rkt  stamp.rkt  time-stamp.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/drracket/repo-time-stamp$ cat ALERT
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/SVG/fonts/Gyre-Termes/Shapes/Regular

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/drracket/repo-time-stamp$ ls -a
.  ..  ALERT  compiled  doc.txt  info.rkt  stamp.rkt  time-stamp.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/drracket/repo-time-stamp$ cd  /usr/share/javascript/mathjax/jax/output/SVG/fonts/Gyre-Termes/Shapes/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/Gyre-Termes/Shapes/Regular$ ls -a
.  ..  .MEMO  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/Gyre-Termes/Shapes/Regular$ cat .MEMO
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{snvxdk2gzuiPZZVv5ytQFaGG0p5.dljM4QDLxMTO0czW}
```

No energy left to explain...
