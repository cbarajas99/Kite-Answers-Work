headers:
  use-splitlines: Use `str.splitlines()`
---
# How to create a list that contains each line of a text file in Python
Creating a list that contains each line of a text file takes every individual line of the text file and makes a Python list out of their string representation.

## Use [`str.splitlines()`](kite-sym:builtins.str.splitlines) to create a list that contains each line of a text file  {#use-splitlines}
Use [`open(file, mode)`](kite-sym:builtins.open) with `file` as the pathname of the file and `mode` as `"r"` to open the file for reading. Call [`file.read()`](kite-sym:builtins.file.read) on `file` to read all of lines in the file. Call [`str.splitlines()`](kite-sym:builtins.str.splitlines) on the previous result to get a list of the lines. After, use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "Line1\nLine2\nLine3"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "r")

lines = a_file.read()
list_of_lists = lines.splitlines()

a_file.close()

print(list_of_lists)
```
