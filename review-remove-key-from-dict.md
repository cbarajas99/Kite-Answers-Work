headers:
  use-dict-pop: Use `dict.pop()`
---
# How to remove a key from a dictionary in Python
Removing a key deletes the `key: value` pair from the dictionary. For example removing `"a"` from `{"a": 1, "b": 2}` results in `{"b": 2}`.

## Use [`dict.pop()`](kite-sym:builtins.dict.pop) to remove a key from a dictionary {#use-dict-pop}

Call [`dict.pop(key)`](kite-sym:builtins.dict.pop) on a dictionary to remove a specified `key` from it.

```python
a_dictionary = {"a": 1, "b": 2}

# removes key "a" along with its value
a_dictionary.pop("a")

print(a_dictionary)
```
