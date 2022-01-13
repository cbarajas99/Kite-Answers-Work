headers:
  use-enumerate: Use `enumerate()`
---
# How to get the line number of a certain phrase in a file in Python
Getting the line number of a certain phrase in a file results in the first line number that the phrase is in.

## Use [`enumerate()`](kite-sym:builtins.enumerate) to get the line number of a certain phrase in a file {#use-enumerate}
Use [`open(file, mode)`](kite-sym:builtins.open) with `file` as the pathname of the file and `mode` as `"r"` to open the file for reading. Call [`enumerate(iterable)`](kite-sym:builtins.enumerate) with `iterable` as the file to get an enumerate object. Use a for-loop to iterate over each line number and line in the enumerate object. At each iteration, use an if-statement to check if the certain phrase is in the line. After, use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "abc\nefg\nhij"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

phrase = "efg"
line_number = "Phrase not found"
a_file = open("sample.txt","r")
for number, line in enumerate(a_file):
  if phrase in line:
    line_number = number
    break

a_file.close()

print(line_number)
```
