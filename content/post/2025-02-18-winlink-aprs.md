---
title: "Winlink and APRS"
subtitle:
date: 2025-02-18
tags: ['winlink', 'btech', 'uvpro', 'aprs']
draft: false
---

I recently added `winlink`
back to my APRS ping
on the UV-PRO.
I immediately got a message from a Winlink gateway
that I had 1 new Winlink message waiting.
For the full RF experience,
I fired up KISS on the UV-PRO
and a session
to K3IR's Winlink gateway (145.030kHz)
and checked my Winlink mail
over the radio.

I needed to be careful to not let HT app start
and re-enable "digital mode"
When "digital mode" is enabled,
it would switch to APRS 144.390MHz
every time WoAD would TX,
and _that_ doesn't work.
The hint was seeing APRS traffic in the WoAD log
while waiting for my Winlink session to initialize.

The email was KC3WRY, Matthew, playing around
sending Winlink via APRS.
I acknowledged and responded to his message.

<!--more-->
