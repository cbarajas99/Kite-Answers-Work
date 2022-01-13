headers:
  use-rstrip(): Use `str.rstrip()`
---
# How to remove whitespace from the end of a string in Python
Removing whitespace from only the end of a string results in a string that excludes whitespace after the last non-whitespace character. For example, removing whitepsace from the end of `" abc "` results in `" abc"`.

## Use [`str.rstrip()`](kite-sym:builtins.str.rstrip) to remove whitespace from the end of a string {#use-rstrip}
Call [`str.rstrip()`](kite-sym:builtins.str.rstrip) to remove whitespace from the end of the string `str`.
```python
a_string = " abc "

no_end_whitespace = a_string.rstrip()

print(no_end_whitespace)
```
