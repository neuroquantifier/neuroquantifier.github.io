---
layout: post
title: tqdm Examples
---
## PyTorch Training Loops

```python
from tqdm import tqdm
from tqdm import trange

# TRAINING LOOP

epochs = 100
#train_loader: PyTorch dataloader for training dataset
#valid_loader: PyTorch dataloader for validation dataset
for epoch in trange(epochs):
    # training
    with tqdm(total=len(train_loader), file=sys.stdout) as pbar:
        for i, (data, label) in enumerate(train_loader):
            ...
            pbar.update(1)
    # validation
    with tqdm(total=len(valid_loader), file=sys.stdout) as vbar:
        for i, (data, label) in enumerate(valid_loader):
            ...
            vbar.update(1)
```

## Python Script (.py)
```python
from tqdm import trange
import time
import sys

for i in trange(10, desc='Epoch'):
    for j in trange(20, leave=False, desc='Loop'):
        time.sleep(0.2)
        
```
