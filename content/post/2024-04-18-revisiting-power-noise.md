---
title: Revisiting Power Noise
subtitle: 
date: 2024-04-18T16:59:56-04:00
tags: ['power', 'noise', 'x6100', 'xiegu', 'battery']
draft: false
---

When I first started
with the X6100,
I'd see some noise
that buried real signals
when plugged
into AC power.

<!--more-->

Running on battery was fine,
and running 
on the external lead-acid 12V battery
was OK too.
For weeks, 
I used the battery
to smooth the noise.
I'd run an AC power supply
in parallel with the battery
and turn it up just high enough
that I didn't see noise in the waterfall.
The battery smoothed the power.

I switched to a LiFePO4 battery,
and I found the built-in charging
circuit made it hard
to balance input power and output power
just right to keep it smooth.

I asked around on the 
[X6100 mailing list](https://groups.io/g/xiegu-x6100/topic/103401251#4578)
and I got 2 suggestions I took:
- a [filter](https://www.amazon.com/dp/B07HTM7Q7F?th=1) I can use 
  with any cheap power supply I already have
- a cleaner, 
  and inexpensive,
  [switching power supply](https://www.mpja.com/12-Volt-Adapter-Power-Supply-5A-Ateck/productinfo/36374+PS/)
  from Ateck that puts out a fixed 12V/5A

I purchased both to try, 
and both helped immensely, 
each on their own.

I wired up the filter 
with some 5525 connectors
and printed a case for it.
I use the filter in combination
with my adjustable 24V/5A power supply
on the go.
That higher-voltage power supply
is also useful
to charge the LiFePO4 battery 
at 14.1V.
The battery also lives in my box 
for portable operation.


I use the Ateck power supply
on my desk by itself
to power the radio at home.
