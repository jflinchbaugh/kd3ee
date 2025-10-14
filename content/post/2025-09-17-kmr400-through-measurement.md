---
title: "KMR400 Through Measurement"
subtitle:
date: 2025-09-17
tags: ['kmr400', 'yagi', 'nanovna', 'w3gms']
draft: false
---

I've been thinking of ways to get more power to W3GMS,
and coax might be the weakest link.
I have about 75ft of RG-58 outside
and maybe 8 ft of RG-174 inside.
I took down the flag pole Yagi
to replace the coax.

I learned how to measure loss
with a "through measurement" on the nanoVNA watching Youtube:
- The old coax run measured at least -6.5dB loss total
  - -4.5dB for the RG-58 by itself
  - -2.0dB for the RG-174 by itself
- The new coax, 100ft of KMR-400, by itself measured -1.5dB,
  and -3.3dB with the patch of RG-174
- SWR sweep of antenna on old coax showed lots of wiggles
  and hung generally low,
  because of all the loss.
- SWR sweep of the antenna with the new coax
  runs much higher on the 100MHz side,
  and takes a nice dip at the resonant frequency.
- Incoming signals look good and strong
  by the S-meter on the TYT-9800

{{< gallery >}}
{{< figure link="/img/2025/2025-09-17-kmr-1.jpg" caption="kmr400" >}}
{{< figure link="/img/2025/2025-09-17-kmr-2.jpg" caption="kmr400 yagi" >}}
{{< /gallery >}}

<!--more-->
