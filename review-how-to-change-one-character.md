headers:
  use-list: Use `list()`
---
# How to change one character in a string in Python
Changing a character in a string replaces it with a different character. To do so, the string must be converted to a mutable data type, like a list. Changing the first character in `"zbc"` to an `"a"` results in `"abc"`.

## Use [`list()`](kite-sym:builtins.list) to construct a mutable list {#use-list}
Call [`list(iterable)`](kite-sym:builtins.list) with a string as `iterable` to construct a mutable list containing each character from the string. Use list indexing to modify the list. Call [`str.join(iterable)`](kite-sym:builtins.str.join) with the empty string `""` as `str` and the modified list as `iterable` to construct a modified string.

```python
a_string = "zbc"

a_list = list(a_string)
# change first character
a_list[0] = "a"
# convert back to string
edited_string = "".join(a_list)

print(edited_string)
```
