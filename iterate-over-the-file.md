headers:
  use-for: Use a for-loop
---
# How to iterate through the lines of a file in Python
Iterating through the lines of a file results in accessing each of the lines separately.

## Use a for-loop to iterate through the lines of a file {#use-for}
In a with-statement, use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Inside the with-statement, use a for-loop to iterate through the lines. Then, call [`str.strip()`](kite-sym:builtins.str.strip) to strip the end-line break from each line.

```python
KITE.set_display_code(False)
text = "This is\nan existing file."
KITE.write_file("sample.txt", text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

with open("sample.txt", "r") as a_file:
  for line in a_file:
    stripped_line = line.strip()
    print(stripped_line)
```
