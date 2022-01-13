headers:
  os-realpath: Use `os.path.realpath()`
  os-dirname: Use `os.path.dirname()`
---
# How to get the path to the current file in Python
Getting the path to the current file will return the absolute path to the current file.

## Use [`os.path.realpath()`](kite-sym:os.path.realpath) to get the path to the current file {#os-realpath}
`__file__` is an attribute that stores the currently running file's name. Call [`os.path.realpath(__file__)`](kite-sym:os.path.realpath) to return the absolute path to the current file.

```python
KITE.start_prelude()
import os
KITE.stop_prelude()

print(os.path.realpath(__file__))
```

## Use [`os.path.dirname()`](kite-sym:os.path.dirname) to get the path to the directory of the current file {#os-dirname}
Call [`os.path.dirname("path_to_file")`](kite-sym:os.path.dirname) to return the absolute path to the directory of the current file. Note that `dirname` accepts a path `string` and not a file name.

```python
KITE.start_prelude()
import os
KITE.stop_prelude()

path_to_file = os.path.realpath(__file__)
print(os.path.dirname(path_to_file))
```
