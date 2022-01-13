headers:
  use-nested-for-loop: Use nested for-loop

---
# How to iterate through a nested list in Python
A nested list is a list containing lists as its elements. Iterating through a nested list iterates through the elements of each inner list.

## Use a nested for-loop to iterate through a nested list {#use-nested-for-loop}

Use a for-loop to iterate through every element of a list. If this list contains other lists, use another for-loop to iterate through the elements in these sublists.

```python
list_of_lists = [[1, 2], [3, 4]]

# Sequentially access each `list`
for list in list_of_lists:
  # Sequentially access each `element`
  for element in list:
   print(element)

```
