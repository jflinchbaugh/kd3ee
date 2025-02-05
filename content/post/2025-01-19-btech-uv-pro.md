---
title: "Btech UV-Pro"
subtitle:
date: 2025-01-19
tags: ['uvpro', 'btech', 'packet', 'aprs']
draft: false
---

### Yet Another Radio
I got interested in AX.25 packet over RF,
so the [Btech UV-Pro](https://baofengtech.com/product/uv-pro/)
immediately looked
like an interesting jumpstart,
when it got a firmware update that allowed
it to operate as a KISS TNC over Bluetooth.

### Application Driven
[HT](https://play.google.com/store/apps/details?id=com.benshikj.ht)
is the up-to-date app for interfacing with the radio.
There's a "BTech Programmer" app,
but it is an older,
branded version of HT.

### Setup
In the radio,
I'd set "General" ->  "Digital" -> "Format" = "APRS",
but the HT app kept switching it back to "BSS" any time
it connected to the radio.
It would never let me set "APRS" until I "verified"
my ham radio callsign.
It wants to do it by sending your license info to some chinese site --
_no thanks_.
Instead, I used a
[web app](https://n5dux.com/ham/aprs-passcode/)
to generated an APRS code that worked in the HT app.

I enabling digital mode
in radio to make it periodically beacon my APRS location.
I set it to a fixed channel for sending APRS.
Only the HT app seems to be able
to set the beacon text for APRS.

I can send messages from radio by prefixing the message with the recipient:
```
KC3WWC-7: hey
```

### TNC KISS Mode
I installed [WoAD](https://woad.sumusltd.com/) on Android,
and enabled TNC KISS on the radio.
I paired the radio to the phone via Bluetooth.
I checked the Winlink RMS map on the website to find nearby packet gateways,
and set the radio to the given packet frequency for the gateway I was trying to use.
I configured a session for the callsign and SSID of the Winlink gateway,
and started the session.
Now it'll send and receive queued email.
There's a log in WoAD that shows what it's doing.

WoAD also has a terminal
which can be used for BBSes,
like [KA3TKW](https://groups.io/g/21repeatergroup).
I connected there
to see some messages and a BBS software from 1990!

[APRSDroid](https://aprsdroid.org/)
can also talk to KISS TNC
over Bluetooth. It's a much nicer UI
than the radio or HT app.
Sometimes when switching apps,
I needed to cycle power on the radio,
but it doesn't usually take too much
to get it going again.

<!--more-->
