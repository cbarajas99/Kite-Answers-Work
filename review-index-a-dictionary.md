headers:
  keys: Index the keys of a dictionary
  values: Index the values of a dictionary
---
# How to index a dictionary in Python
In versions of Python 3.7 or greater, dictionaries are order-preserving. Indexing a dictionary accesses the key or value at that index. For example, the key and value at index `0` in `{"a": 1, "b": 2}` are `"a"` and `1` respectively.

## Use [`list()`](kite-sym:builtins.list) to index the keys of a dictionary {#keys}
Call [`list(*args)`](kite-sym:builtins.list) with a dictionary as `*args` to return a list of the keys. Use the indexing syntax `list[index]` to return the key at `index` in `list`.

```python
a_dictionary = {"a": 1, "b": 2}

# convert dictionary to list
keys_list = list(a_dictionary)
a_key = keys_list[0]

print(a_key)
```

## Use [`dict.values()`](kite-sym:builtins.dict.values) and [`list()`](kite-sym:builtins.list) to index the values of a dictionary {#values}
Call [`dict.values()`](kite-sym:builtins.dict.values) to return a collection of the values of `dict`. Call [`list(*args)`](kite-sym:builtins.list) with this collection as `*args` to return a list of the values in the dictionary. Use the indexing syntax `list[index]` to return the value at `index` in `list`.

```python
a_dictionary = {"a": 1, "b": 2}

values = a_dictionary.values()
# convert dictionary values to list
values_list = list(values)
a_value = values_list[0]

print(a_value)
```

> **Further reading:**
> Lists support an indexing syntax to access their elements. You can read more about list indexing [here](https://docs.python.org/3/tutorial/introduction.html#lists).
