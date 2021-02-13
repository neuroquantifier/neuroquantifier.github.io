---
layout: post
title: PyTorch DataParallel
tags: pytorch
---

## Send Model to DataParallel

```python
# model: nn.Module PyTorch model

if torch.cuda.device_count() > 1:
    print(f"Let's use {torch.cuda.device_count()} GPUs!")
    parallelized_model = nn.DataParallel(model)
    
    # see how data gets split
    for data in valid_loader:
        input = data.to(device)
    output = parallelized_model(input)
    print("Outside: input size", input.size(),
          "output_size", output.size())
```
