headers:
  use-split: Use `str.split()`
---
# How to cut a string in Python
Cutting a string results in a list that contains the string before and after each cut as items. For example, splitting `"hello world"` on the whitespace results in `["hello", "world"]`.

## Use [`str.split()`](kite-sym:builtins.str.split) to cut a string {#use-split}
Call [`str.split(sep)`](kite-sym:builtins.str.split) with `sep` as the character that will split the string.
```python
a_string = "hello world"

split_string = a_string.split(" ")

print(split_string)
```

> **Further Reading:**
> There are more ways to split a string with [`str.split()`](kite-sym:builtins.str.split), read [here](https://kite.com/python/docs/__builtin__.str.split) to learn more.
