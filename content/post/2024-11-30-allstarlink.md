---
title: "AllStarLink"
subtitle:
date: 2024-11-30
tags: ['allstarlink', 'uhf', 'w3gms', 'digital', 'uvk5']
draft: false
---

I finally got my AllStarLink 3
node up and running.
I had registered for a node number,
and I had bought the pieces.
The Pi Zero W boards wouldn't boot,
so I used a Pi 4 that I have laying around
with the USB radio device I purchased a while ago.


### Initial Installation on Pi 4
I started out with the
[official instructions](https://allstarlink.github.io/user-guide/pi-detailed/):
- Downloaded the image for the Pi
- Installed the Pi Imager by deb file
  instead of just `dd`ing it to the device,
  since the imager conveniently allows pre-configuring:
  - user
  - locale
  - WiFi network

### Configured the Cheap Ausinc UHF AllStar Radio Dongle
I purchased the [hardware](https://www.amazon.com/dp/B0BPHJQ1BJ)
from Amazon a while ago.
It has a USB-C port,
and the cable is flipped for different modes:
- one way to program the frequency via USB serial
- other way to use the USB sound device for TX/RX
The product description mentioned the different modes,
but I didn't recognize it.
I learned about the flip from a
[video](https://www.youtube.com/watch?v=PPte1TwMxXI)

I downloaded the `srfrs.py`
[Python script](https://github.com/jumbo5566/SRFRS)
to the Pi,
and used it to configure frequency and tone
to protect default access to it:
`./srfrs.py --port /dev/ttyUSB0 --frequency 438.1 --ctcss 94.8`
Matthew, KC3WRY, suggested this frequency in the 70cm of the band.
I was reading and wondering about 446.1 or 433 or so.

### More Configuration and Confirmation
I followed [another video](https://www.youtube.com/watch?v=aeuj-yI8qrU)
for more configuration and confirmation
of the settings from intro video.

I made another pass at web-based configs and `asl-menu`.
I set it to be a `SimpleUSB` device
in simplex mode,
and I tuned the volume settings.
I had no TX until I set "Change CTCSS From = no".
I don't know what that setting does, but
the tip came from the video.
Then I could use the `allmon3` web interface
to connect up to Parrot+ node (55553)
for testing,
and it reported, "volume just about right."
I could connect and disconnect to nodes from the web interface.
There are other commands in the web interface
to say the time or id the node on demand.

I could send DTMF commands
from my UV-K5
with the F4HWN firmware:
- `*` starts DTMF entry, PTT sends the codes.
- `*1 <node number>` disconnects from a node
- `*2 <node number>` connects to monitor another node
- `*3 <node number>` connects to transcieve to another node
- other scripts, like "disconnect all" don't seem to work yet.

The W3GMS admins granted me access to connect
my node to the repeater,
so I'll have a chance to try it out there.
I was also able to connect to [K3IR](https://k3ir.org/).

<!--more-->
