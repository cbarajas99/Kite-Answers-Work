headers:
  use-sorted: Use `sorted()`
---
# How to sort a dictionary by its values in Python
Sorting a dictionary by its value results in a new dictionary that is sorted by its values in increasing order. For example, sorting `{"a": 2, "b": 4, "c": 3, "d": 1}` results in `{'d': 1, 'a': 2, 'c': 3, 'b': 4}`.

## Use [`sorted()`](kite-sym:builtins.sorted) to sort a dictionary by its values {#use-sorted}
Create an initially empty dictionary. Call [`sorted(iterable, key)`](kite-sym:builtins.sorted) with `iterable` as the dictionary that will be sorted and `key` as `key = original_dict.get` to get a list of keys from `original_dict` that are. Use a for-loop to iterate through the previous result. At each iteration, in the new dictionary, assign the key to the value it had in the original dictionary.

```python
original_dict = {"a": 2, "b": 4, "c": 3, "d": 1}

new_dict = {}
for key in sorted(original_dict, key = original_dict.get):
  new_dict[key]  = original_dict[key]

print(new_dict)
```
