headers:
  use-in: Use the `in` keyword
---
# How to get a line count of a file in Python
Getting a line count of a file returns the number of nonempty lines in the file.

## Use the `in` keyword to get a line count of a file {#use-in}
Use [`open(file, mode)`](kite-sym:builtins.open) with the filename as `file` and `"r"` as `mode` to open a file and read its contents. Use a for-loop and the `line in file` syntax to check if `line` is nonempty. Increase line count by 1 each time `line` is nonempty. Use [`file.close()`](kite-sym:builtins.file.close) with the filename as `file` to close the file.
```python
KITE.set_display_code(False)
text = "Hello\n\nWorld\n"
KITE.write_file("sample.txt", text)
KITE.set_display_code(True)

file = open("sample.txt", "r")
line_count = 0
for line in file:
    if line != "\n":
        line_count += 1
file.close()

print(line_count)
```
Use a list comprehension for a more compact implementation. Use [`len()`](kite-sym:builins.len) to get the number of nonempty lines in the file.
```python
KITE.set_display_code(False)
text = "Hello\n\nWorld\n"
KITE.write_file("sample.txt", text)
KITE.set_display_code(True)

file = open("sample.txt", "r")
# line.strip("\n") removes "\n"
nonempty_lines = [line.strip("\n") for line in file if line != "\n"]
line_count = len(nonempty_lines)
file.close()

print(line_count)
```

> **Further reading:**
> List comprehensions provide a concise way to create lists. [Read more about list comprehensions here.](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions).
