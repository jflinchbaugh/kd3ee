---
title: "Next Firmware: F4HWN"
subtitle:
date: 2024-11-21
tags: ['f4hwn', 'aubsuk', 'quansheng', 'uvk5']
draft: false
---

### Problem: AUBSUK multiple scan list
The scan lists aren't combining correctly on AUBSUK firmware.
It's skipping entries based on ordering.
I realized I was missing most of simplex channels,
but seeing the GMRS channels,
when I enabled my "simplex" scan list in combo with primary repeaters.
There's an existing [issue logged](https://github.com/AubsUK/uv-k5-firmware-custom/issues/29),
but it's hard to describe and to reproduce,
I think.

### Trying the Next Firmware, F4HWN 3.7
[F4HWN](https://github.com/armel/uv-k5-firmware-custom)
is available on GitHub.
I loaded it on both radios in place of AUBSUK
to see how I get along.
I've found a few features I really like:
- Scan on start:
  if it's scanning when I switch it off,
  it'll scanning when switched on.
- 3 scan lists: 1, 2, 3, 123, 0, all
  - they don't recombine as freely, but I have:
    - simplex, repeaters, satellites on 1
    - GMRS on 3
- scan is just as fast as others, so we'll see if it's tolerable.
- "main only" display is nice, much easier to read.
- spectrum analyzer with scan range,
  but I can't assign it to a button.
  - Fn-5 is only way to activate it.

I think the S-meter is calibrated much differently from AUBSUK,
and other firmwares I've loaded,
[calibration for VHF/UHF vs HF](https://github.com/armel/uv-k5-firmware-custom/issues/81),
The S-meter seems to read higher than I expect with lots of S9+.

The spectrum analyzer with a range seems wonky at times:
it may be scanning the entire range, but the graph doesn't seem all there.
I noticed it with the scan of 144MHz-148MHz.

<!--more-->
