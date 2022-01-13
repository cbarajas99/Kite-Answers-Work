headers:
  use-in: Use the `in` keyword
  use-set-difference: Use `set.difference()`
  use-symmetric-difference: Use `set.symmetric_difference()`
---
# How to get the difference between two list in Python
Getting the difference between two lists results in a list containing the items that are in the first list but not the second. For instance, the difference between `[1, 2, 4]` and `[4, 5, 6]` is `[1, 2]`. Getting the symmetric difference between two lists results in a list containing items from either lists but not both. For instance, the symmetric difference between `[1, 2, 4]` and `[4, 5, 6]` is `[1, 2, 5, 6]`.

## Use the `in` keyword to get the difference between two lists {#use-in}
Use a for-loop to iterate through the first list. Use the syntax `item not in list` to check if `item` is not in the second list. Append `item` to a new list if it is not in the second list.
```python
list1 = [1, 2, 4]
list2 = [4, 5, 6]

list_difference = []
for item in list1:
  if item not in list2:
    list_difference.append(item)

print(list_difference)
```
Use a list comprehension for a more compact implementation.
```python
list1 = [1, 2, 4]
list2 = [4, 5, 6]

list_difference = [item for item in list1 if item not in list2]

print(list_difference)
```
## Use [`set.difference()`](kite-sym:builtins.set.difference) to get the difference between two lists {#use-set-difference}
Use [`set()`](kite-sym:builtins.set) to convert both lists into sets. Use [`set.difference(s)`](kite-sym:builtins.set.differnce) where `set` is the first set and `s` is the second set to get the difference between both sets. Use [`list()`](kite-sym:builtins.list) to convert the set difference into a list.
```python
list1 = [1, 2, 4]
list2 = [4, 5, 6]

set_difference = set(list1) - set(list2)
list_difference = list(set_difference)

print(list_difference)
```
## Use [`set.symmetric_difference()`](kite-sym:builtins.set.symmetric_difference) to get the symmetric difference between two lists {#use-symmetric-difference}
Use [`set()`](kite-sym:builtins.set) to convert both lists into sets. Use [`set.symmetric_difference(s)`](kite-sym:builtins.set.symmetric_difference) where `set` is the first set and `s` is the second set to get the symmetric difference between both sets. Use [`list()`](kite-sym:builtins.list) to convert the set symmetric difference into a list.
```python
list1 = [1, 2, 4]
list2 = [4, 5, 6]

difference = set(list1).symmetric_difference(set(list2))
list_difference = list(difference)

print(list_difference)
```
