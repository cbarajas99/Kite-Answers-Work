headers:
  use-chdir: Use `os.chdir()`
---
# How to change the current directory in Python
Changing the current directory results in moving to a different directory to access different things.

## Use [`os.chdir()`](kite-sym:os.chdir) to change the current directory {#use-chrdir}
Call [`os.chdir(path)`](kite-sym:os.chdir) with `path` as the full path of the desired directory to change the current directory.
```python
KITE.start_prelude()
import os
KITE.stop_prelude()

# shows current directory
print(os.getcwd())

os.chdir("/kite/")

# shows directory after changing
current_directory = os.getcwd()
print(current_directory)
```
