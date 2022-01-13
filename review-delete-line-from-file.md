headers:
  use-del: Use `del`
  use-for-loop: Use a for loop
---
# How to delete a line from a file in Python
Deleting a line from a file returns a file with all the lines except the removed line. This can be done with or without knowing the index of the line. For example, deleting a line `line2` from a file containing `line1\nline2\nline3\n` will return `line1\nline3\n`.

## Use a for loop to delete a line from a file where its position is unknown {#use-for-loop}
Open a file to read with [`open("file", "r")`](kite-sym:builtins.open). Use [`file.readlines()`](kite-sym:builtins.file.readlines) to create a list where each element is a line from the file. Close the file. Open the file again to write with [`open("file", "w")`](kite-sym:builtins.open). Use a for-loop to iterate through the list of lines, and use the syntax `line in lines` to look for the line that is going to be deleted. Use [`file.write()`](kite-sym:builtins.file.write) to write all lines except the deleted line to the file.

```python
KITE.set_display_code(False)
text = "line1\nline2\nline3\n"
KITE.write_file('sample.txt', text)
KITE.set_display_code(True)

# get list of lines
a_file = open("sample.txt", "r")
lines = a_file.readlines()
a_file.close()

# overwrite lines in file
new_file = open("sample.txt", "w")
for line in lines:
    if line.strip("\n") != "line2":
        new_file.write(line)

new_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
## Use [`del`](kite-symbuiltins.del) to delete a line from a file where its position is known {#use-del)
Open the file for reading and use [`file.readlines()`](kite-sym:builtins.file.readlines) to create a list where each element is a line from the file. Use the syntax `del list[index]` with `list` as the list of lines to delete the element at `index`. Write the edited list of lines to a file to create a new file without the deleted line.

```python
KITE.set_display_code(False)
text = "line1\nline2\nline3\n"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

# get list of lines
a_file = open("sample.txt", "r")
lines = a_file.readlines()
a_file.close()

# delete lines
del lines[1]

# write to file without line
new_file = open("sample.txt", "w+")
for line in lines:
    new_file.write(line)

new_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
