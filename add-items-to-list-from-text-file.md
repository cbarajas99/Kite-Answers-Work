headers:
  use-strip: Use `file.strip()`
---
# How to put a text file into a list in Python
Putting a text file into a list results in a list with each element as a line in the file.

## Use to add items from text file into a list {#use-strip}
Call [`open(file, mode)`](kite-sym:builtins.open) with the path of a file as `file` and `mode` as `"r"` to open the file for reading. Use a for-loop to iterate each through each line in the file. At each iteration, call [`str.strip()`](kite-sym:builtins.str.strip) with `str` as the current line to remove excess whitespace from `str`, and call [`list.append(object)`](kite-sym:builtins.list.append) with `object` as the stripped line to append it to the initially empty `list`.

```python
KITE.set_display_code(False)
text = "Dave\nGeorge\nSamuel"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

file = open("sample.txt", "r")
lines_list = []
for line in file:
  stripped_line = line.strip()
  lines_list.append(stripped_line)

print(lines_list)
```
