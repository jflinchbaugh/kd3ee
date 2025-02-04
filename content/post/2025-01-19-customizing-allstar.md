---
title: "Customizing Allstar"
subtitle:
date: 2025-01-19
tags: ['allstarlink']
draft: false
---

Customizing actions of the ASL node
isn't all that complicated.
Everything can be setup in `/etc/asterisk/rpt.cfg`
under the `[functions]` section:
- added `*77` to announce IP to help find it
  on DHCP on WIFI (hotspot):
  ```
  77 = cmd,asl-say -n 63047 -w ip4
  ```
- added `*78` to shutdown the node via DTMF
  ```
  78 = cmd,shutdown now
  ```
- ensured I could disconnect all with `*6`
  ```
  6 = ilink,6
  ```
- made the node fire that `*77` command on startup
  by adding to the `(node-main)` section for my node:
  ```
  startup_macro = *77
  ```

<!--more-->
