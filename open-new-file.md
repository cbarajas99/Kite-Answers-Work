headers:
  use-write: Use the file mode `w`
---
# How to open and create a new file with write mode in Python
Opening a file with write mode creates a new file if that file does not already exist.

## Use the file mode `w` to create a new file {#use-write}
Use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"w"` to open a new `file` in write mode. If `file` is an existing file, it will be overwritten. Call [`file.write(data)`](kite-sym:builtins.file.write) to write `data` to the new file. Use [`file.close()`](kite-sym:builtins.file.close) to close the file.

```python
a_file = open("sample.txt", "w")
a_file.write("This is a new file.\n")
a_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
