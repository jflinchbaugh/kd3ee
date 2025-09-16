---
title: "Allstar Link Macros"
date: 2025-05-15
tags: ["allstarlink", "macros", "ham radio"]
---
I finally got my reboot command working correctly
on my Allstar node:
```
79 = cmd,shutdown -r now
```

I also set up a convenient shortcut
to connect to the 985 Allstar node.
Now, instead of typing out the full connection string,
I can simply dial `*51*` to connect.
The macro definition for this is:

```
[macros]
1 = *353085
```

And to make things even easier,
I configured `*6`
as a quick way to disconnect
from all active connections.

<!--more-->
