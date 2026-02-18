---
title: "Automatic Allstar Link to 985"
subtitle:
date: 2026-01-12
tags: ['985', 'w3gms', 'allstar']
draft: false
---

I updated `rpt.conf` on my node
to enable the `813` DTMF code
for making permanent link.
The _permanent link_ will try to re-establish itself
after a disconnect.

It doesn't re-establish upon reboot,
so a macro is still needed on startup.
I updated the existing startup macro to `*81353085`
after `*77` (report).

<!--more-->
