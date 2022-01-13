headers:
  use-rstrip: Use `str.rstrip()`
---
# How to remove end-line breaks from lines read from a text file in Python
Removing end-line breaks from lines when reading a text file ignores the breaks on the end of each line.

## Use [`str.rstrip()`](kite-sym:builtins.str.rstrip) to remove end-line breaks from lines read from a text file {#use-rstrip}
Use [`open(file, mode)`](kite-sym:builtins.open) with `file` as the pathname of the file and `mode` as `"r"` to open the file for reading. Use a for-loop to iterate through each line in the file. At each iteration, call [`str.rstrip()`](kite-sym:builtins.str.rstrip) to remove the line break at end of the line. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "abc\nefg\nhij\n"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "r")

string_without_line_breaks = ""
for line in a_file:
  stripped_line = line.rstrip()
  string_without_line_breaks += stripped_line
a_file.close()

print(string_without_line_breaks)
```
