---
title: "X6100 Firmware Again"
subtitle:
date: 2024-09-23
tags: ['xiegu', 'x6100', 'firmware']
draft: false
---

Xiegu released another updated firmware for the X6100:
APP 1.1.9 & BASE 1.1.8, dated 2024-09-23.
1. I downloaded it from Radioddity, and wrote it to an SD card:
  ```
  $ sudo dd if=sdcard.img of=/dev/sda bs=1M status=progress
  ```

2. I booted the new card for the app upgrade to 1.1.9,
3. I applied baseband 1.1.8 from the menu in the UI.
4. I tried the CW key in the stock firmware, and it transmitted
  (unlike last time).
5. I booted back to R1CBU, and it looked good there as well.

I did a little FT8,
decoded some CW,
and listened to some SSB on 40m.
I found I could to turn the RF Gain closer to 100
instead of below 63.
It may be reading slightly lower power on the display before ALC kicks in:
up to but not over the 5W, where it used to often push a little past.

It'll stay.
<!--more-->
