headers:
  use-split: Use `str.split()`
---
# How to convert each line in a text file into a list in Python
Converting each line in a text file results in a list of lists where each list is a line from the text file.

## Use [`str.split()`](kite-sym:builtins.str.split) to convert each line in a text file into a list {#use-split}
Use [`open(file, mode)`](kite-sym:builtins.open) with `file` as the pathname of the file and `mode` as `"r"` to open the file for reading. Create a for-loop to iterate through each line of the file. At each iteration, call [`str.strip()`](kite-sym:builtins.str.strip) on the line to remove line breaks, and then call [`str.split()`](kite-sym:builtins.str.split) on the stripped line to create a list of the words in the line. Call [`list.append(line)`](kite-syn:builtins.list.append) with `line` as the previous list to add it to the initially empty list of lists. After, use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "This file\nwill\nbe converted to a list"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "r")

list_of_lists = []
for line in a_file:
  stripped_line = line.strip()
  line_list = stripped_line.split()
  list_of_lists.append(line_list)

a_file.close()

print(list_of_lists)
```
Use a list comprehension for a more compact implementation.
```python
KITE.set_display_code(False)
text = "This file\nwill\nbe converted to a list"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "r")

list_of_lists = [(line.strip()).split() for line in a_file]

a_file.close()

print(list_of_lists)
```
