headers:
  use-pop: Use `dict.pop()`
---
# How to rename a dictionary key in Python
Renaming a dictionary key modifies a key-value pair to have a new key, the same value, and its location at the end of the dictionary. For example, renaming `"a"` to `"A"` in `{"a": 1, "B": 2, "C": 3}` results in `{'B': 2, 'C': 3, 'A': 1}`.

## Use [`dict.pop()`](kite-sym:builtins.dict.pop) to rename a dictionary key {#use-pop}
Call [`dict.pop(key)`](kite-sym:builtins.dict.pop) to remove an old `key` from `dict` and return its value. With the same dictionary, assign a new dictionary key to this value.

```python
a_dict = {"a": 1, "B": 2, "C": 3}

new_key = "A"
old_key = "a"
a_dict[new_key] = a_dict.pop(old_key)

print(a_dict)
```
