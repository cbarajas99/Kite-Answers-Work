headers:
  use-parent: Use `pathlib.PurePath.parent`
---
# How to get the parent directory in Python
Getting the parent directory results in the full path of the parent directory of a file or directory. For instance, getting the parent directory of `/path/to/file/sample.txt` results in `/path/to/file`.

## Use [`pathlib.PurePath.parent`](kite-sym:pathlib.PurePath.parent) to get the parent directory {#use-parent}
Call [`pathlib.PurePath(*pathsegments)`](kite-sym:pathlib.PurePath) with a full path of a directory or file as `*pathsegments` to make a filesystem path. Use [`pathlib.PurePath.parent`](kite-sym:pathlib.PurePath.parent) with the previously made filesystem path as `pathlib.PurePath` to get the parent directory.
```python
KITE.start_prelude()
import pathlib
KITE.stop_prelude()

a_path = pathlib.PurePath("/path/to/file/sample.txt")
parent_directory = a_path.parent

print(parent_directory)
```
