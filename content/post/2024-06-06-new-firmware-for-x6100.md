---
title: New Firmware for X6100
subtitle:
date: 2024-06-07T23:44:38-04:00
tags: ['x6100', 'firmware', 'r1cbu']
draft: false
---

### a header at h3

There's a new person
building onto Oleg's R1CBU firmware.
He first made a [patch TGZ available](https://groups.io/g/xiegu-x6100/topic/105905552),
and then an [entire image](https://groups.io/g/xiegu-x6100/message/5330).

He has a [repo for this work](https://github.com/gdyuldin/x6100_gui),
and it includes some build instructions which reference the buildroot
and submodules.
I think I'm close to being able to build it,
but I'm seeing some errors trying
to find the `xkbcommon` headers.

I did patch his source with my DB changes.
I built the DB: `sqlite3 params.db < params.sql`,
mounted the `DATA` partition,
and copied my custom params.db to it.

It's looking nice so far.
I can use `flrig`
and have `wsjtx` and `fldigi`
both talk to it simultaneously.
That's the main improvement in my mind,
but it includes some other nice improvements.

<!--more-->
