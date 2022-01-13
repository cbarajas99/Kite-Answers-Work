headers:
  use-range: Use `range()`
---
# How to make a list of n-lists in Python
Making a list of n-lists results in a list with n-items where each item is the same list. For instance, making a list containing 5 lists with each list being `[1,2]` results in `[[1, 2], [1, 2], [1, 2], [1, 2], [1, 2]]`.

## Use [`range()`](kite-sym:builtins.range) to make a list of n-lists in Python {#use-range}
Use [`range(start, stop)`](kite-sym:builtins.range) where `start` is 0 and `stop` is the desired amount of lists within the list. Use a for-loop to iterate through this range. In each iteration, use [`list.append(item)`](kite-sym:builtins.list.append) where `list` is an initially empty list and `item` is another list.
```python
list1 = []
list2 = [1,2]
n = 5

for x in range(0,n):
  list1.append(list2)

print(list1)
```
Use a list comprehension for a more compact implementation.
```python
list2 = [1,2]
n = 5

list1 = [list2 for x in range(0,n)]

print(list1)
```
