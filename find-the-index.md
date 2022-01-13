headers:
  use-in: Use the `in` keyword
  use-list-index: Use `list.index()`
---
# How to find the index of an item in a list in Python
Finding the index of an item in a list returns a list containing all the indices of an item in a list. For example, finding the indices of `a` in `[a, b, a]` returns `[0, 2]`.

## Use the `in` keyword to find the index of an item in a list {#use-in}
Use a for-loop to iterate through the list. Use the syntax `(index, item) in list` and [`enumerate(list)`](kite-sym:builtins.enumerate) to check if `item` is the specific item, then add the index to a new list.

```python
a_list = ["a", "b", "a"]
indices_of_a = []
for (index, item) in enumerate(a_list):
  if item == "a":
    indices_of_a.append(index)
print(indices_of_a)
```
Use list comprehension for a more compact implementation.
```python
a_list = ["a", "b", "a"]
print([index for (index , item) in enumerate(a_list) if item == "a"])
```
## Use [`list.index()`](kite-sym:builtins.list.index) to find the index of the first occurrence of an item in a list {#use-list-index}
Call [`list.index(value)`](kite-sym:builtins.list.index) to find the index of the first occurrence of `value` in `list`.

```python
a_list = ["a", "b", "c"]
index_of_element = a_list.index("b")
print(index_of_element)
```
