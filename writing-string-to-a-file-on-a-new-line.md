headers:
  use-newline: Use the newline character
---
# How to write a string to a file on a new line every time in Python
Writing a string to a file on a new line returns a new file with multiple lines of strings.

## Use the newline character to write a string to a file on a new line every time {#use-newline}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"w"` to open the file for writing. Call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as a string containing the newline character `"\n"` as its last character to write a line to `file` and to create a new line for the next written string. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
file = open("sample.txt", "w")
file.write("Hello\n")
file.write("World\n")
file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
