headers:
  use-join: Use `str.join()`
---
# How to combine some elements in a list of strings in Python
Combining some elements in a list of strings results in a shorter list of strings where one element is the result of combining some elements of the previous list.

## Use [`str.join()`](kite-sym:builtins.str.join) to merge some items in a list of strings {#use-join}
Call [`str.join(iterable)`](kite-sym:builtins.str.join) with `str` as `""` and `iterable` as the part of the list to merge into one item. Use list slicing to rassign `[x]` to the same part of the string with `x` as the previous result.

```python
a_list = ["a", "b", "c", "d"]
# only works for list of strings
merged_items = ''.join(a_list[1:3])
a_list[1:3] = [merged_items]

print(a_list)
```
