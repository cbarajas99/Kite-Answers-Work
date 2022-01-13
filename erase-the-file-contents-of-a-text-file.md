headers:
  use-w-mode: Use the file writing mode
  use-truncate: Use `file.truncate()`
---
# How to erase the file contents of a text file in Python
Erasing the file contents of a text file will result in an empty text file.

## Use the file writing mode to erase the file contents of a text file {#use-w-mode}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"w"` to open the file for writing. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
KITE.set_display_code(False)
text = "Hello\nWorld\n"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

file = open("sample.txt","w")
file.close()

KITE.set_display_code(False)
file = open("sample.txt","w")
file.write(" ")
file.close()
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
## Use [`file.truncate()`](kite-sym:builtins.file.truncate) to erase the file contents of a text file {#use-truncate}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"r+"` to open the file for reading and writing. Call [`file.truncate(size)`](kite-sym:builtins.file.truncate) with `size` as 0. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "Hello\nWorld\n"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

file = open("sample.txt","r+")
file.truncate(0)
file.close()

KITE.set_display_code(False)
file = open("sample.txt","w")
file.write(" ")
file.close()
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
