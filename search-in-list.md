headers:
  use-in: Use the `in` keyword
---
# How to find an item in a list in python
Searching for an item in a list results in `True` if the item is in the list and `False` otherwise. For instance, searching for `3` in `[4, 5, 6]` results in `False`.

## Use the `in` keyword to find an item in a list {#use-in}
Use the syntax `item in list` to determine if `item` is contained in `list`.
```python
a_list = [4, 5, 6]

boolean = 3 in a_list

print(boolean)
```
To find all elements that satisfy a certain condition, iterate through the list and store each item in a new list if the condition is satisfied.
```python
a_list = [4, 5, 6]

less_than_6 = []
for item in a_list:
  if item < 6:
    less_than_6.append(item)

print(less_than_6)
```
Use a list comprehension for a more compact implementation.
```python
a_list = [4, 5, 6]

less_than_6 = [item for item in a_list if item < 6]

print(less_than_6)
```
