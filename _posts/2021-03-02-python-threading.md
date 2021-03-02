---
layout: post
title: python threading 
---
## Python Threading 

Outline: Define a function, then initiate it as a thread.

```python
import threading 

#define a function to run as a separate thread here
def my_function(function_args):
	pass

new_thread = threading.Thread(target=my_function, args=(function_args,), daemon=True)
new_thread.start()

```
