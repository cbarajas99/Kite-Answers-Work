headers:
  use-writelines: Use `file.writelines()`
---
# How to add lines to an existing file in Python
Adding lines to an an existing file results in the same file with new lines added at the end.

## Use [`file.writelines()`](kite-sym:builtins.file.writelines) to add lines to existing file {#use-writelines}
Use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"a"` to open `file` for appending. Call [`file.writelines(sequence_of_strings)`](kite-sym:builtins.file.writelines) with `sequence_of_strings` as a list of strings with `\n` at the end of each string to add lines to the file. After, use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.set_display_code(False)
text = "This file\nis an\nexisting file.\n"
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

a_file = open("sample.txt", "a")

sequence_of_strings = ["These are\n", "new lines.\n"]
a_file.writelines(sequence_of_strings)

a_file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
