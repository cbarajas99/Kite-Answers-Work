headers:
  use-dict-items: Use `dict.items()`
  use-dict-keys: Use `dict.keys()`
  use-dict-values: Use `dict.values()`
---
# How to iterate over the keys and values of a dictionary in Python
A dictionary stores key-value pairs. Iterating over a dictionary accesses its keys and values individually.

## Use [`dict.items()`](kite-sym:builtins.dict.items) to iterate over the keys and values of a dictionary {#use-dict-items}
Use a for-loop with two variables and iterate through [`dict.items()`](kite-sym:builtins.dict.items) to access the keys and values of a dictionary.

```python
a_dictionary = {"a": 1, "b": 2}

# iterates over the keys and values of a_dictionary
for key, value in a_dictionary.items():
    print(key, value)
```

## Use [`dict.keys()`](kite-sym:builtins.dict.keys) to iterate over the keys of a dictionary {#use-dict-keys}
Use a for-loop and iterate through [`dict.keys()`](kite-sym:builtins.dict.keys) to access the keys of a dictionary.

```python
a_dictionary = {"a": 1, "b": 2}

# iterates over the keys of a_dictionary
for key in a_dictionary.keys():
    print(key)
```

## Use [`dict.values()`](kite-sym:builtins.dict.keys) to iterate over the values of a dictionary {#use-dict-values}
Use a for-loop and iterate through [`dict.values()`](kite-sym:builtins.dict.values) to access the values of a dictionary.

```python
a_dictionary = {"a": 1, "b": 2}

# iterates over the values of a_dictionary
for value in a_dictionary.values():
    print(value)
```
