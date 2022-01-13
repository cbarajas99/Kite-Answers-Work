headers:
  use-replace: Use `str.replace()`
---
# How to replace a string within a file in Python
Replacing a string within a file modifies the file to replace specific strings with new strings.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to replace a string within a file {#use-replace}
Use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Use a for-loop to iterate through the lines of the file. At each iteration, call [`str.strip()`](kite-sym:builtins.str.strip) to strip the end-line break. Then call [`str.replace(old, new)`](kite-sym:builtins.str.replace) to replace `old` with `new` in the line. After, concatenate this new string with `"\n"` to add an end-line break. Add the resultant string to the string created in the previous iteration of the for-loop. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`. Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname with `mode` as `"w"` to open `file` for writing. Call [`file.write(str)`](kite-sym:builtins.file.write) with `str` as the new file contents to overwrite the old file contents. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
KITE.set_display_code(False)
text = "Replace all of \nold string\nwith new string\nin this file\nuntil all old string read new string"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

reading_file = open("sample.txt", "r")

new_file_content = ""
for line in reading_file:
  stripped_line = line.strip()
  new_line = stripped_line.replace("old string", "new string")
  new_file_content += new_line +"\n"
reading_file.close()

writing_file = open("sample.txt", "w")
writing_file.write(new_file_content)
writing_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
