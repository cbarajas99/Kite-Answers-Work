headers:
  use-write: Use `file.write()`
---
# How to append a newline to a file in Python
Appending a newline to a file that does not contain a end-line break writes `"\n"` after the file contents.

## Use [`file.write()`](kite-sym:builtins.file.write) append a newline to a file {#use-write}
In a with-statement, use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"a"` to open `file` for appending. Inside the with-statement, call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as `"\n"` to append a newline to `file`. Then, call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as a string with an end-line break to write `data` on a new line.

```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

new_line = "This new line will be added.\n"

with open("sample.txt", "a") as a_file:
  a_file.write("\n")
  a_file.write(new_line)

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
