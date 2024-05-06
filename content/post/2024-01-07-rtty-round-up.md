---
title: RTTY Round-Up
subtitle: 
date: 2024-01-07
tags: ['rtty', 'hf', 'arrl', 'contest', 'r1cbu', 'flrig', 'fldigi']
draft: false
---

I participated in the 
[RTTY Round-Up](https://contests.arrl.org/ContestRules/RTTY-RU-Rules.pdf).

### Trouble with fldigi/R1CBU

I screwed around lots trying to get `fldigi` talking to the radio.
R1CBU software works great with `wsjt-x`,
but `fldigi` and `flrig` 
completely failed to connect.
It wouldn't key the radio.
Switching back to stock software on the radio worked fine with `flrig`,
but where's the fun in that.

For `flrig`, 
I could tell it 
that it was an older version 
of the radio (X5105?),
and it would key and set frequency,
but `flrig` wouldn't read back the frequency
when updated at the radio.

I ultimately got `fldigi` talking to R1CBU 
by using `flcat` with an [xml file
for G106](https://sourceforge.net/projects/fldigi/files/xmls/xiegu/).

Then I could "tune" power output following 
[instructions in `fldigi` manual](http://www.w1hkj.com/FldigiHelp/audio_adjust_page.html).

### Working!

I started making some contacts on 10M and 15M.
It's much more like voice contacts: 
yelling back and forth on the same channel.
I'm using macros 
and sticking to those for the contest.
They're on the 3rd page of macros in `fldigi`.

I've made at least a few contacts, 
so I'll submit them to the contest

<!--more-->
