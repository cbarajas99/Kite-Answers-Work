headers:
  use-readlines: Use `file.readlines()`
---
# How to edit a specific line in a text file in Python
Editing a specific line in a text file changes the contents of a line located at specific index, leaving all other lines in the file unchanged.

## Use [`file.readlines()`](kite-sym:builtins.file.readlines) to edit a specific line in text file {#use-readlines}
Use [`open(file, mode)`](kite-sym:builtins.open) with `file` as the pathname of the file and `mode` as `"r"` to open the file for reading. Call [`file.readlines()`](kite-sym:builtins.file.readlines) to get a list containing each line in the opened `file`. Use list indexing to edit the line at a certain line number. Call [`open(file, mode)`](kite-sym:builtins.open) again with `file` as the pathname of the file and `mode` as `"w"` to open the file for writing. Use [`file.writelines(sequence_of_strings)`](kite-sym:builtins.file.writelines) with `sequence_of_strings` as the list containing the lines to overwrite the file. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "Line1\nChange This Line\nLine3"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "r")
list_of_lines = a_file.readlines()
list_of_lines[1] = "Line2\n"

a_file = open("sample.txt", "w")
a_file.writelines(list_of_lines)
a_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
