---
title: "Bug Scanning on Aubs 00.07"
subtitle:
date: 2024-07-23
tags: ['quansheng', 'ht', 'firmware', 'aubs', 'bug', 'scanning']
draft: false
---

I have my UV-K5 and UV-K6
running [aubs 00.07 firmware](https://github.com/AubsUK/uv-k5-firmware-custom/releases/tag/v00.07).
I added a simplex frequency (446.100MHz)
to use as with my local cross-band repeater
in position 110.
I added the new channel to scan list 1.

Upon powering on the radio,
I could scan lists 1 (local repeaters)
and 4 (satellites) together.
When I press the up arrow
to advance off an active channel,
the scan would now skip list 1,
and go right to 4,
and continue to skip list 1.
Before I realized it was happening,
I thought the day was super quiet.

I dropping the repeater frequency from scan list 1,
and the scanning behaved correctly.
I tried removing _another_ channel from scan list 1,
and reintroducing channel 110 to the list,
but that didn't fix it,
so it's not an issue with the count.

Much of scan list 1 is lower in the channels,
so I moved my new repeater frequency from channel 110
to position 30,
right after all my other simplex channels.
That seems to work fine,
so that's how I'm leaving it.

I may need to try some more things
and figure out a reproduction to file a bug
on the project:
- Is it something about the frequency of 460.100?
- Or is channel 110 the problem?
- Would another frequency in that spot be a problem?
- Are there other channels that would trigger the issue?

<!--more-->
