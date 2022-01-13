headers:
  use-del: Use the `del` keyword and the desired key is known
  use-del2: Use the `del` keyword and the desired key is unknown
---
# How to remove an item from a dictionary in Python
Removing an item from a dictionary results in the same dictionary without one key-value pair. For example, removing the key `"two"` or value `2` from `{"one": 1, "two" : 2, "three": 3}` results in `{'one': 1, 'three': 3}`.

## Use the `del` keyword to remove an item from a dictionary and the desired key to remove is known {#use-del}
Call [`dict.keys()`](kite-sym:builtins.dict.keys) to get a list of the keys of `dict`. Create a for-loop to iterate through the list of keys. At each iteration, check if the key is the desired key to remove. If it is, use the `del` keyword along with dictionary indexing to delete the key-value pair and then call the `break` keyword.
```python
a_dictionary = {"one": 1, "two" : 2, "three": 3}

desired_key = "two"
for key in a_dictionary.keys():
  if key == desired_key:
    del a_dictionary[key]
    break

print(a_dictionary)
```
## Use the `del` keyword to remove an item from a dictionary and the desired key to remove is unknown {#use-del2}
Call [`dict.items()`](kite-sym:builtins.dict.keys) to get a list of the key-value pairs of `dict`. Create a for-loop to iterate through the list of key-value pairs. At each iteration, check if the value is the desired value to remove. If it is, use the `del` keyword along with dictionary indexing to delete the key-value pair and then call the `break` keyword.
```python
a_dictionary = {"one": 1, "two" : 2, "three": 3}

desired_value = 2
for key, value in a_dictionary.items():
  if value == desired_value:
    del a_dictionary[key]
    break

print(a_dictionary)
```
