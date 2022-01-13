headers:
  use-clear: Use `list.clear()`
  use-del: Use the `del` keyword
  set-to-empty: Set the entire list to an empty list
---
# How to delete all the items in a list in Python
Deleting all the items in a list results in an empty list. For example, deleting all the items in `[1, 2, 3, 4]` results in `[]`.

## Use [`list.clear()`](kite-sym:builtins.list.clear) to delete all the items in a list {#use-clear}
Call [`list.clear()`](kite-sym:builtins.list.clear) on the list to delete all the items in the list.

```python
a_list = [1, 2, 3, 4]

a_list.clear()

print(a_list)
```

## Use the `del` keyword to delete all the items in a list {#use-del}
Call the `del` keyword followed by the indexing of the entire list to delete all the items in the list.

```python
a_list = [1, 2, 3, 4]

del a_list[:]

print(a_list)
```

## Set the entire list to an empty list to delete all the items in a list {#set-to-empty}
Index the entire list and set it to equal an empty list.

```python
a_list = [1, 2, 3, 4]

a_list[:] = []

print(a_list)
```
