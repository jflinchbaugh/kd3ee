---
title: "RFI in the Car"
subtitle:
date: 2025-06-02
tags: ['rfi', 'mobile', '985', 'spectrum', 'uv-k5', 'quansheng']
draft: false
---

I was out mobile,
but I couldn't check-in
to the 985 Workbench.
I had a weak signal,
and I got a boost
in interference when car powered off.
It was mostly through the mobile antenna/coax,
and it was enough to drown out W3GMS.
I confirmed with spectrum analyzer on UV-K5.

I also had my AllStar 3 node
but it wouldn't connect either.
The node connected
to my phone hotspot fine,
and it got an IP and all that.
I could use the web interface or DTMF,
but DTMF was flaky/slow.
While debugging,
I connected to the parrot node (55553) fine,
but I only got "connection failed"
from W3GMS (53085).
I connected to W3GMS fine from home network the next morning.

{{< gallery >}}
{{< figure link="/img/2025/2025-06-02-spectrum-1.jpg" caption="car on" >}}
{{< figure link="/img/2025/2025-06-02-spectrum-2.jpg" caption="car off" >}}
{{< /gallery >}}

<!--more-->
