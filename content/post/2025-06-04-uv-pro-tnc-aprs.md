---
title: "UV-Pro, TNC, and APRS"
subtitle:
date: 2025-06-04
tags: ['aprs', 'tnc', 'btech', 'uvpro']
draft: false
---

[APRSDroid](https://aprsdroid.org/)
would often fail to reconnect to the UV-PRO:
  `java.io.IOException: read failed, socket might closed or timeout, read ret: -1`
The [HT](https://play.google.com/store/apps/details?id=com.benshikj.ht&hl=en_US)
app would manage to reconnect OK.
I would need to cycle power on the radio to get APRSDroid
to reconnect.
In APRSDroid,
Preferences->Connection Preferences->Channel was set to `1`.
I blanked that channel setting,
and now it may be reconnecting
between stop and start of app,
bluetooth,
or distance.

As a side note,
having the UV-PRO monitoring
a frequency other than APRS
may interfere with packet reception.
I don't see as many APRS packets
when monitoring another repeater,
probably due to interruptions from the non-APRS audio.

<!--more-->
