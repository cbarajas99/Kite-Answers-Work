headers:
  use-if-else: Use an if-else block
  use-indexing: Use indexing
---
# How to replace a line in a file in Python
Replacing a line in a file results in an identical file being created with a specified line being different.

## Use an if-else block to replace a line in a file {#use-if-else}
In a with-statement, use [`open(original_file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `original_file` for reading. Inside the with-statement, in another with-statement, use [`open(new_file, mode)`](kite-sym:builtins.open) with `mode` as `"w"` to open `new_file` for writing. Inside this with-statement, create a for-loop to iterate through the lines of `original_file`.

At each iteration, use an if-else block to check if the line is the line to replace. If it's, call [`file.write(str)`](kite-sym:builtins.file.write) with `str` as the new line to write the new line to `new_file`. If it's not, call [`file.write(str)`](kite-sym:builtins.file.write) with `str` as the original line to write the line to `new_file`.
```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("original.txt", text)
KITE.display_file("original.txt")
KITE.set_display_code(True)

original_line = "an existing file."
new_line = "a new file."

with open("original.txt", "r") as original_file:
  with open("new.txt", "w") as new_file:
    for line in original_file:
      if line == original_line:
        new_file.write(new_line)
      else:
        new_file.write(line)

KITE.set_display_code(False)
KITE.display_file("new.txt")
KITE.set_display_code(True)
```

## Use indexing to replace a line in a file {#use-indexing}
In a with-statement, use [`open(original_file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `original_file` for reading. Inside the with-statement, in another with-statement, use [`open(new_file, mode)`](kite-sym:builtins.open) with `mode` as `"w"` to open `new_file` for writing. Inside this with-statement, create a for-loop to iterate through the lines of `original_file`.

At each iteration, use an if-else block to check if the line number is the line number of the line to replace. If it's, call [`file.write(str)`](kite-sym:builtins.file.write) with `str` as the new line to write the new line to `new_file`. If it's not, call [`file.write(str)`](kite-sym:builtins.file.write) with `str` as the original line to write the line to `new_file`.
```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("original.txt", text)
KITE.display_file("original.txt")
KITE.set_display_code(True)

line_number = 2
new_line = "a new file."

line_count = 1
with open("original.txt", "r") as original_file:
  with open("new.txt", "w") as new_file:
    for line in original_file:
      if line_count == line_number:
        new_file.write(new_line)
      else:
        new_file.write(line)
      line_count += 1

KITE.set_display_code(False)
KITE.display_file("new.txt")
KITE.set_display_code(True)
```
