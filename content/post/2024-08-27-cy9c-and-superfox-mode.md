---
title: "CY9C and SuperFox Mode"
subtitle:
date: 2024-08-27
tags: ['cy9c', 'dxpedition', 'superfox', 'wsjtx']
draft: false
---

### CY9C St Paul Island Expedition

Someone spotted
[CY9C's Saint Paul Island Expedition](https://t-rexsoftware.com/cy9c/)
on the 21 mailinglist:
18095kHz, SuperFox FT8 mode.
I tuned my `WSJTX` to the frequency,
enabled SuperHound,
and it crashed upon trying to decode.

```
  Running: /usr/bin/jt9 -s WSJT-X -w 1 -m 3 -e /usr/bin -a /home/john/.local/share/WSJT-X -t /tmp/WSJT-X
  sh: 1: /usr/bin/sfrx: not found
  Fortran runtime error: EXECUTE_COMMAND_LINE: Invalid command line

  Error termination. Backtrace:
  #0  0x7f02d8e21b9a in ???
  #1  0x7f02d8e22699 in ???
  #2  0x7f02d8e22afc in ???
  #3  0x7f02d90b8eeb in ???
  #4  0x7f02d90b9099 in ???
  #5  0x559f9788ca06 in ???
  #6  0x559f97885f15 in ???
  #7  0x559f97885467 in ???
  #8  0x559f978838a2 in ???
  #9  0x7f02d883edb9 in __libc_start_call_main
    at ../sysdeps/nptl/libc_start_call_main.h:58
  #10  0x7f02d883ee74 in __libc_start_main_impl
    at ../csu/libc-start.c:360
  #11  0x559f97883900 in ???
  #12  0xffffffffffffffff in ???
```

I filed a
[bug for the missing binary](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1079942).
In the meantime,
I downloaded and installed the `wsjtx deb` file
from sourceforge to make the DX QSO.
I saw them again on 14.094MHz, but they don't hear me.

I checked in on the bug,
and the maintainer explained
that those binaries are not open source,
so not included with the Debian package.
To fix it longer-term,
I kept the new binaries,
and went back to the package
that Debian provided.

<!--more-->
