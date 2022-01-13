headers:
  use-write: Use `file.write()`
---
# How to write a line to a file in Python
Writing a line to a file appends the line to the end of the file.

## Use [`file.write()`](kite-sym:builtins.file.wwrite) to write a line to a file {#use-write}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"a+"` to open the file for appending. Call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as a string containing the newline character `"\n"` as its last character to write a line to `file`. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
KITE.set_display_code(False)
text = "Hello\n"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

file = open("sample.txt", "a+")
file.write("World\n")
file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
