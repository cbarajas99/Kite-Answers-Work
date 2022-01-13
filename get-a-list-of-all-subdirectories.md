headers:
  use-os-walk: Use `os.walk()`
---
# How to get a list of all subdirectories in the current directory in Python
Getting a list of all subdirectories in the current directory results in a list
containing the full paths of all the subdirectories.

## Use [`os.walk()`](kite-sym:os.walk) to get a list of all subdirectories in the current directory {#use-os-walk}
Call [`os.walk(path)`](kite-sym:os.walk) with `path` as the full path of the current directory to generates the file names in a directory tree. Use a for-loop and Use the syntax `subdirectory in directory tree` to iterate through `directory tree`. Use indexing to append the first element in `subdirectory` to a new list.
```python
KITE.start_prelude()
import os
KITE.stop_prelude()

subdirectories = []
directory_tree = os.walk("/kite/run")
for subdirectory in os.walk("/kite/run"):
  # subdirectory[0] contains the full path of the subdirectory
  subdirectories.append(subdirectory[0])

print(subdirectories)
```
Use a list comprehension to get a more compact implementation.
```python
KITE.start_prelude()
import os
KITE.stop_prelude()

directory_tree = os.walk("/kite/run")
subdirectories = [subdirectory[0] for subdirectory in directory_tree]

print(subdirectories)
```
