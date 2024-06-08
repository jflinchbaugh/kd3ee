---
title: 985 Workbench Net - 2024-05-20
subtitle:
date: 2024-05-21T08:56:22-04:00
tags: ['985', 'w3gms', 'workbench', 'antenna']
draft: false
---

### My Week in radio

#### The Vertical EFHW

I Tested my 20m EFHW wire and unun
on 2 different POTA outings
In an inverted v with a counterpoise, it worked pretty well,
but could be shortened.
As a vertical, the SWR was higher,
and the counterpoise made it worse.
I compared the vertical EFHW
to the trusty old EFRW
in a mostly vertical configuration.
That one had exhibited a terrible SWR
as well with or without counterpoise.
Maybe I needed more radials instead of a counterpoise?
I have 2 ARRL antenna books, basic and the big one,
so I could read, I suppose.
During these experiments,
my computer experienced some common-mode interference too.

#### Custom Antenna Winder

I 3D-printed a nice customized winder with the transformer attached.
I modified the code to be parameterized to any size I want.

#### More VHF

I've been discovering I can hear some further repeaters
using the spectrum analyzer feature on my Quansheng,
so I've been adding more repeaters to the scan.

### Thoughts on My Vertical Antenna Problem

- You can tune and end-fed at one angle,
  and it can have a different swr at another angle.
- They're sensitive to objects in their near field.
  Is the unun near ground or branches?
  The same goes for the other end of the antenna.
  Try changing the orientation.
- The ends are high-voltage, so they're sensitive to capacitance.
  The middle is high-current, low-voltage.
- Vertical antenna will have very different conditions at each end.
  inverted-V or horizontal will have more similar conditions at each end.
- RF comes from the current in the middle.
  - Vertical is an inexact science.
  - The tree effects it.
  - 50ft of coax helps provide RF ground, 
  and less can be a problem.
- Watch height of unun.
- The Smith chart on the NanoVNA can help evaluate what's happening.
  - Crossover point on the chart can show the tuning and the swr
  - Is it environmental or the wire?
- Counterpoise placement can be sensitive.
- Add radials for vertical.

### Interesting Bits from Other People

- Tim, W3QP, did the W2 SOTA campout: 6 summits and 32 contacts, mostly VHF.
- Chuck, NA3CW, talked about accomplishing an 75M net using online WebSDRs
  to hear, because propagation was so bad.
- Rob, K3VIL, is having fun with his QRP IC-705.

<!--more-->
