headers:
  idx: Use `list.index()` and `max()`
---
# How to find the index of the maximum value of a list in Python
Finding the index of the maximum value of a list first finds the maximum value of the list, then returns the index of that value. For example, the index of the maximum value in `[3, 2, 1]` is `0`.

## Use [`list.index()`](kite-sym:builtins.list.index) and [`max()`](kite-sym:builtins.max) to find the index of the maximum value of a list {#idx}
Call [`max(iterable)`](kite-sym:builtins.max) with a list as `iterable` to find the maximum value of the list. Call [`list.index(value)`](kite-sym:builtins.list.index) with the maximum value as `value` to get the index of the maximum value.
```python
a_list = [3, 2, 1]

# get max value of list
max_value = max(a_list)
# get index of max value
max_index = a_list.index(max_value)

print(max_index)
```
