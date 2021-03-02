---
layout: post
title: Python Threading & Multiprocessing
---

## Threading, Multiprocessing, and Asyncio

CPU intensive tasks should use **multiprocessing**, and I/O bound tasks like downloading should use **asyncio**.


### Threading

```python
from threading import Threading

#define a function to run as a separate thread here
def my_function(function_args):
	pass

new_thread = Thread(target=my_function, args=([function_arg1, function_arg2]), daemon=True)
new_thread.start()

```

### Multiprocessing

```python
from multiprocessing import Process

define my_function(function_args):
	pass

new_process = Process(target=my_function, args([function_arg1]))
new_process.start()

#test to see if process is running
print(f"Process is alive: {new_process.is_alive()}")

# get process id (pid)
# call from inside process.
print(f"Process id: {os.getpid()})

# get parent process id (ppid)
print(f"Parent process id: {os.getppid()}")


