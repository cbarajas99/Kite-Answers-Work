headers:
  use-getcwd: Use `os.getcwd()`
---
# How to get the current directory in Python
Getting the current directory results in a full path of the directory that a file is in.

## Use [`os.getcwd()`](kite-sym:os.getcwd) to get the current directory {#use-getcwd}
Call [`os.getcwd()`](kite-sym:os.getcwd) to get the current directory of the file.
```python
KITE.start_prelude()
import os
KITE.stop_prelude()

current_directory = os.getcwd()

print(current_directory)
```
