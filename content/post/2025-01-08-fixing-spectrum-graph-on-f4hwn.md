---
title: "Fixing the Spectrum Graph on F4HWN"
subtitle:
date: 2025-01-08
tags: ['f4hwn', 'quansheng', 'code']
draft: false
---

There was a bug for a while
in F4HWN 3.9 on the Quansheng radios.
The spectrum analyzer graph was
[too narrow](https://github.com/armel/uv-k5-firmware-custom/issues/322)
when number of bars exceded 128.
I'd easily run into the problem when I set the scan range
to 144.000MHz to 148.000MHz,
and activate the spectrum analyzer.

I dug into the code a bit and fixed it,
so now it scales for large and small ranges.

I submitted a
[pull request](https://github.com/armel/uv-k5-firmware-custom/pull/352)
to the project, and it was accepted and merged
to be included in the F4HWN 4.0 release.
Until that release, I'll be running my custom build.

I also made a change to allow me to map the spectrum analyzer
to a programmable side button like AubsUK had,
but I'm no longer convinced it's worth
the limited code space it would consume
in the binary.

{{< gallery >}}
{{< figure link="/img/2025/2025-01-08-spectrum.jpg" caption="spectrum analyzer working" >}}
{{< /gallery >}}

<!--more-->
