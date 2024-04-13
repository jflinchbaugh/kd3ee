---
title: VHF Reception
subtitle: 
date: 2024-03-19
tags: ['985', 'w3gms', 'vhf', 'antenna', 'dipole', 'troubleshooting']
draft: false
---

### Reception Problems
During 985 net on Monday night,
which is VHF on my UV-K5 running egzumer 0.22.0,
I'd get periodic static
in reception.
It got bad enough to completely cut-out.
I was using my simple wire dipole hanging 
in the tree outside.

K3IR had been frustratingly quiet as well,
so I checked the antenna with the NanoVNA
as it hung outside.
There were no fluctuations in SWR,
so it's not connections or proximity.

I tried the Explorer QRZ-1 HT,
and it sounded great 
on the same antenna on the same net.
Is my UV-K5 broken?

To test a bit further,
I ordered a new UV-K6 to compare.
I also downgraded to egzumer 0.21.0
for further testing.

The next day, 
Tuesday morning,
K3IR was sounding better,
but I was getting the same periodic noises.
The outside antenna doesn't completely cut out,
but shows terrible doubling/overload 
as if from FM station.

Inside, 
the magmount antenna 
on the 3d printer is better.
Is the dipole outside too sensitive 
and bringing in more signal than
the frontend of the UV-K5 can handle?
