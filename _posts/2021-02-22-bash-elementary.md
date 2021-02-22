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


## User Input Arguments

Simplest format: $n, where n is nth argument (separated by spaces)
```bash
echo 'First Argument:' $1
echo 'Second Argument:' $2
```

Args are stored in list $@, which can be iterated through:
```bash
args=("$@")
echo "First Arg: ${args[0]}, Second Arg: ${args[1]}"
```

Show whole list of args:
```bash
echo $@
```

**Length of list of args**:
```bash
echo Number of arguments passed: $#
```

