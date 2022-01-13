headers:
  use-items: Use [`dict.items()`](kite-sym:builtins.dict.items)
---
# How to remove a key-value pair from a dictionary when the key is unknown in Python
Removing a key-value pair from a dictionary when the key is unknown results in a new dictionary without the specified key-value pair.

## Use [`dict.items()`](kite-sym:builtins.dict.items) to remove a key-value pair from a dictionary when the keys is unknown {#use-items}
Use [`dict.items()`](kite-sym:builtins.dict.items) to get a list of `key, value` tuples from the dictionary `dict`. Use a for-loop to iterate through each `key, value` pair in the list. At each iteration, use an if-statement to check if `value` equals the value to remove. If it doesn't, use `dict[key] = value` to add the current `key, value` pair to a new dictionary `dict`.
```python
a_dictionary = {"a": 1, "b" : 2, "c": 3}

remove_value = 2
result_dictionary = {}
for key, value in a_dictionary.items():
  if value != remove_value:
    result_dictionary[key] = value

print(result_dictionary)
```
Use a dictionary comprehension for a more compact implementation.
```python
a_dictionary = {"a": 1, "b" : 2, "c": 3}

remove_value = 2
result_dictionary = {key: value for key, value in dict1.items() if value != remove_value}

print(result_dictionary)
```
