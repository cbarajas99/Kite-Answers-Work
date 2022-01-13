headers:
  use-keys: Use `dict.keys()`
---
# How to calculate the difference in keys between two dictionaries in Python
Calculating the difference in keys from two dictionaries results in the set of keys contained in the larger dictionary but not the smaller dictionary. For example, the difference between `{"a": 1, "b": 2, "c": 3, "d": 4}` and `{"b": "two", "d": "four"}` results in `{'c', 'a'}`.

## Use [`dict.keys()`](kite-sym:builtins.dict.keys) to calculate the difference in keys between two dictionaries {#use-keys}
Call [`dict.keys()`](kite-sym:builtins.dict.keys) on the larger dictionary to get a copy of the dictionary's list of keys. Repeat this step  with the second dictionary. Subtract the keys of the smaller dictionary from the keys of the other dictionary to get a set of the difference in keys.
```python
dict1 = {"a": 1, "b": 2, "c": 3, "d": 4}
dict2 = {"b": "two", "d": "four"}

keys1 = dict1.keys()
keys2 = dict2.keys()
difference = keys1 - keys2

print(difference)
```
