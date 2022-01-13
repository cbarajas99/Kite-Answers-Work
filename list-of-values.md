headers:
  use-values: Use `dict.values()`
---
# How to get a list of values from a dictionary in Python
Getting a list of values from a dictionary results in a list that contains all the values of the dictionary. For example, the list of values for `{"a": 1, "b": 2, "c": 3}` is `[1, 2, 3]`.

## Use [`dict.values()`](kite-sym:builtins.dict.values) to get a list of values {#use-values}
Call [`dict.values()`](kite-sym:builtins.dict.values) to get the values of the dictionary. Use [`list(object)`](kite-sym:builtins.list) with `object` as the values of the dictionary to convert it into a list.
```python
a_dict = {"a": 1, "b": 2, "c": 3}

values = a_dict.values()
values_list = list(values)

print(values_list)
```
