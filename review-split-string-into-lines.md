headers:
  use-splitlines: Use `str.splitlines()`
---
# How to split a multi-line string into lines in Python
Splitting a multi-line string into lines returns a list of the lines in the string. For example, splitting `"ab\nc"` returns `["ab", "c"]`.

## Use [`str.splitlines()`](kite-sym:builtins.str.splitlines) to split a string into lines {#use-splitlines}
Call [`str.splitlines()`](kite-sym:builtins.str.splitlines) to split a multi-line string `str` into a list of lines.

```python
a_string = "ab\nc"

# excludes line break for each line
lines = a_string.splitlines()

print(lines)
```
