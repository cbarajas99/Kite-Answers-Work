headers:
  use-dict-fromkeys: Use `dict.fromkeys()`
  use-set: Use `set()`
---
# How to remove duplicates from a list in Python
A duplicate is an element that appears more than once in a list. For example, `2` is a duplicate in `[1, 2, 2]`.

## Use [`set()`](kite-sym:builtins.set) to remove duplicates from a list {#use-set}
Call [`set(*args)`](kite-sym:builtins.set) with a list as `*args` to create a set containing the unique elements of the list. Use [`list(*args)`](kite-sym:builtins.list) with the new set as `*args` to convert back to a list.

```python
a_list = [1, 2, 2]

# sets have unique elements
a_set = set(a_list)
# convert set to list
no_duplicates = list(a_set)

print(no_duplicates)
```

## Use the [`dict.fromkeys()`](kite-sym:builtins.dict.fromkeys) to remove duplicates from a list {#use-dict-fromkeys}
If maintaining the order of the elements is necessary, call [`dict.fromkeys(iterable)`](kite-sym:builtins.dict.fromkeys) with a list as `iterable` to create a dictionary containing the unique elements of the list as keys. Use [`list(*args)`](kite-sym:builtins.list) to with the new dictionary as `*args` to convert back to a list containing only the keys.

```python
a_list = [1, 2, 2]

# dictionaries contain unique keys
a_dictionary = dict.fromkeys(a_list)
# convert dictionary to list
no_duplicates = list(a_dictionary)

print(no_duplicates)
```
