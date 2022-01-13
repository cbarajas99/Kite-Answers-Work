headers:
  use-getcwd: Use `getcwd()`
---
# How to get current path in Python
Getting the current path returns a string representing the current working directory.

## Use [`os.getcwd()`](kite-sym:os.getcwd) to get current path
Use [`os.getcwd()`](kite-sym:os.getcwd) to get the full path of the current file's directory.

```python
KITE.start_prelude()
import os
KITE.stop_prelude()

current_directory = os.getcwd()

print(current_directory)
```
