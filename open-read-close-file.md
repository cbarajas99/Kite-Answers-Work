headers:
  use-with: Use a with-statement
  use-open-read-close: Use `open()`, `file.read()`, and `file.close()`
---
# How to open, read, and then close a file in Python
Opening, reading, and then closing a file results in the file being accessed, displayed, and saved respectively.

## Use a with-statement to open, read, and then close a file {#use-with}
In a with-statement, use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Inside the with-statement, call [`file.read()`](kite-sym:builtins.file.read) to read the entire `file`. Using a with-statement closes the file when exiting the with-block.

```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("sample.txt", text)
KITE.set_display_code(True)

with open("sample.txt", "r") as a_file:
  print(a_file.read())
```
## Use [`open`()](kite-sym:builtins.open), [`file.read()`](kite-sym:builtins.file.read), and [`file.close()`](kite-sym:builtins.file.close) to open, read, then close a file {#use-open-read-close}
Use [`open`(file, mode)](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Call [`file.read()`](kite-sym:builtins.file.read) to read the entire `file`. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("sample.txt", text)
KITE.set_display_code(True)

a_file = open("sample.txt", "r")
print(a_file.read())
a_file.close()
```
