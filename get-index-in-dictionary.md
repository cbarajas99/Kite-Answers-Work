headers:
  use-index: Use `list.index()`
---
# How to get the index of a key from a dictionary in Python
 Getting the index of a key in a dictionary results in the index of the key in the list of dictionary keys. For example, getting the index of `"b"` in `{"a": 1, "b": 2, "c": 3}` results in 1.

## Use [`list.index()`](kite-sym:builtins.list.index) to get the index of a key from a dictionary in Python {#use-index}
Use [`list(object)`](kite-sym:builtins.list) with `object` as the dictionary to convert it to a list. Call [`list.index(object)`](kite-sym:builtins.list.index) on the previous list to get the index of the key `object`.
```python
a_dict = {"a": 1, "b": 2, "c": 3}

key = "b"
dict_to_list = list(a_dict)
index = dict_to_list.index(key)

print(index)
```
