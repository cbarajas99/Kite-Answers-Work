headers:
  use-for-loop: Use a for loop
---
# How to remove multiple items from a list in Python
Removing multiple elements from a list results in a new list excluding those elements. For example, removing the elements in `[1, 3]` from the list `[1, 2, 3, 4]` results in `[2, 4]`.

## Use a for-loop to remove multiple items from a list {#use-for-loop}
Use a for-loop to iterate through the original list. Use `if element not in list` to check if `element` is not in the list of elements to remove `list`. If it is not, use ['list.append(object)'](kite-sym:builtins.list.append) to add `object` to an initially empty list.

```python
original_list = [1, 2, 3, 4]
elements_to_remove = [1, 3]

filtered_list = []
for element in original_list:
    if element not in elements_to_remove:
        # adding elements that are not to be removed
        filtered_list.append(element)

print(filtered_list)
```
Use a list comprehension for a more compact solution.

```python
original_list = [1, 2, 3, 4]
elements_to_remove = [1, 3]

filtered_list = [element for element in original_list if element not in elements_to_remove]

print(filtered_list)
```
