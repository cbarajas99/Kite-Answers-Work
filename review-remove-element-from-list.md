headers:
  use-del: Use `del`
  use-list-remove: Use `list.remove()`
---
# How to remove an element from a list in Python
Removing an element deletes the element from the list. For example, removing `"c"` from `["a", "b", "c"]` results in `["a", "b"]`.

## Use [`list.remove()`](kite-sym:builtins.list.remove) to remove an element from a list {#use-list-remove}
Call [`list.remove(x)`](kite-sym:builtins.list.remove) on a list to remove the first occurrence of `x`.

```python
a_list = ["a", "b", "c"]

# remove a specific element
a_list.remove("c")

print(a_list)
```

## Use `del` to remove an element at a specific index {#use-del}
Use `del` followed by `list[i]` to remove the element at index `i` from `list`.

```python
a_list = ["a", "b", "c"]

# remove element based on index
del a_list[2]

print(a_list)
```
