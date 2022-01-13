headers:
  use-if-else: Use if-else statements
---
# How to split a list based on a condition in Python
Splitting a list based on a condition results in two lists where one list contains items that satisfies the condition and another list for those that don't. For example, when splitting `[1, 2, 3, 4]` based on items being even, it results in `[2, 4]` for the even list, and `[1, 3]` for the odd list.

## Use if-else statements to split a list based on condition {#use-if-else}
Create a for-loop to iterate through the items of the list. Use an if-statement to check if the item satisfies the condition, and then add it to the an initially empty list. Use an else-statement to add the item that does not satisfy the condition to different initially empty list.
```python
a_list = [1, 2, 3, 4]

even = []
odd = []
for item in a_list:
  if item % 2 == 0:
    even.append(item)
  else:
    odd.append(item)

print(even)
print(odd)
```
Use a list comprehension for a more compact implementation.

```python
a_list = [1, 2, 3, 4]

even = [item for item in a_list if item % 2 == 0]
odd = [item for item in a_list if item % 2 != 0]

print(even)
print(odd)
```
