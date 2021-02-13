---
layout: post
title: Vanilla PyTorch Template
---
## PyTorch Rhythm

Useful for testing add-ons and plugins without needing to start up a big model.

```python
import torch
from torch import nn, optim

# Data
data = torch.rand(10, 2)
label = torch.rand(10, 1)

# Model
class Model(nn.Module):
    def __init__(self):
        super().__init__()
        self.linear1 = nn.Linear(2,4)
        self.relu = nn.ReLU()
        self.linear2 = nn.Linear(4,1)
    def forward(self, x):
        x = self.linear1(x)
        x = self.relu(x)
        x = self.linear2(x)
        return x
        
model = Model()

# Loss Function and Optimizer
criterion = torch.nn.MSELoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.01)

# Training Loop
for epoch in range(10):
    label_pred = model(data)
    loss = criterion(label_pred, label)
    optimizer.zero_grad()
    loss.backward()
    optimizer.step()
    
    print(f'Loss: {loss}')
    
```
