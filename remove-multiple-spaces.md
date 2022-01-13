headers:
  use-split: Use `str.split()`
---
# How to remove multiple spaces in a string in Python
Removing multiple spaces from a string results in a string having a single space in between words.

## Use [`str.split()`](kite-sym:builtins.str.split) to remove multiple spaces in a string {#use-split}
Call [`str.split()](kite-sym:str.split) to split the `str` at space and save into a list. Use [`str.join(iterable)`](kite-sym:str.join) where `str` is `" "` and `iterable` is the list contain the split string.
```python
a_string = "hello  world"

single_spaces = " ".join(a_string.split())

print(single_spaces)
```
