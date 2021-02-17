---
layout: post
title: Bash Script Elements 
---
## Datetime 

```bash
#!/user/bin/bash

DATETIME=$(date "+%Y-%m-%d %H:%M:%S")
LINUX_EPOCH=$(date "+%s")
echo It is now: $DATETIME
echo The Linux Epoch started $LINUX_EPOCH seconds ago.
```

