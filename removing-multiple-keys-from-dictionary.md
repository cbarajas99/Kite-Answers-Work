headers:
  use-del: Use `del`
  use-pop: Use `dict.pop()`
---
# How to remove multiple keys from a dictionary in python
Removing multiple keys from a dictionary results in a dictionary that does not contain those key-value pairs that were removed. For example, removing
the keys `one` and `three` from `{"one": 1, "two": 2, "three": 3, "four": 4}` results in `{'two': 2, 'four': 4}`.

## Use `del` to remove multiple keys from a dictionary {#use-del}
Create a for-loop to iterate through the list of keys that are to be removed from the dictionary. At each iteration, call `del` along with dictionary indexing to delete the key-value pair.
```python
a_dictionary = {"one": 1, "two": 2, "three": 3, "four": 4}

keys_to_remove = ["one", "three"]
for key in keys_to_remove:
  del a_dictionary[key]

print(a_dictionary)
```
```python
a_dictionary = {"one": 1, "two": 2, "three": 3, "four": 4}

keys_to_remove = ["one", "three"]
new_dictionary = {del a_dictionary[key] for key in keys_to_remove}

print(new_dictionary)
```
## Use [`dict.pop()`](kite-sym:builtins.dict.pop) to remove multiple keys from a dictionary {#use-pop}
Create a for-loop to iterate through the list of keys that are to be removed from the dictionary. At each iteration, call [`dict.pop(key)`](kite-sym:builtins.dict.pop) with `key` as the key to be removed from `dict.`.
```python
a_dictionary = {"one": 1, "two": 2, "three": 3, "four": 4}

keys_to_remove = ["one", "three"]
for key in keys_to_remove:
  a_dictionary.pop(key)

print(a_dictionary)
```
