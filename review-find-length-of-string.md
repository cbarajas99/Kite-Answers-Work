headers:
  use-len: Use `len()`
---
# How to find the length of a string in Python
A string is a sequence of characters. The length of a string is the number of characters. For example, the length of `"abc"` is `3`.

## Use [`len()`](kite-sym:builtins.len) to find the length of a string {#use-len}
Call [`len(object)`](kite-sym:builtins.len) with `object` as the string to get its length.
```python
a_string = "abc"

# get length of a_string
string_length = len(a_string)

print(string_length)
```
