headers:
  use-dict-keys-collection: Use `dict.keys()` to print a collection
  use-dict-keys-loop: Use `dict.keys()` with a for loop
---
# How to print the keys of a dictionary in Python
A dictionary stores key-value pairs. Printing the keys of a dictionary outputs every key it has.

## Use [`dict.keys()`](kite-sym:builtins.dict.keys) to print a collection of dictionary keys {#use-dict-keys-collection}
Call [`dict.keys()`](kite-sym:builtins.dict.keys) to return a view of the keys of the dictionary.

```python
a_dictionary = {"a": 1, "b": 2}

# gets all the keys of a_dictionary
keys = a_dictionary.keys()

print(keys)
```

## Use [`dict.keys()`](kite-sym:builtins.dict.keys) with a for loop to print the keys of a dictionary {#use-dict-keys-loop}
Use a for loop to iterate over [`dict.keys()`](kite-sym:builtins.dict.keys). Print each key within the loop.

```python
a_dictionary = {"a": 1, "b": 2}

for key in a_dictionary.keys():
    # prints each key seperately
    print(key)
```
