headers:
  use-del: Use `del`
  use-pop: Use `list.pop()`
---
# How to remove the first element from a list in Python
Removing the first element from a list results in a new list without the first element. For example, removing the first element from `[1, 2, 3]` results in `[2, 3]`.

## Use the `del` keyword to remove the first element from a list {#use-del}
Use the `del` keyword and the slicing notation `[0]` to access and remove the first element from a list.

```python
a_list = [1, 2, 3]

# deletes the first element
del a_list[0]

print(a_list)
```

## Use [`list.pop()`](kite-sym:builtins.list.pop) to remove the first element from a list {#use-pop}
Call [`list.pop(index)`](kite-sym:builtins.list.pop) on a list with `index` as `0` to remove and return the first element.

```python
a_list = [1, 2, 3]

# removes the first element
popped_element = a_list.pop(0)

print(a_list)
print(popped_element)
```
