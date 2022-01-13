headers:
  use-in: Use the `in` keyword
---
# How to find an element in a list of tuples in Python
Finding an element in a list of tuples returns a list of tuples containing that element. For example, finding `2` in `[(1, 2), (3, 4), (2, 4)]` returns `[(1, 2), (2, 4)]`.

## Use the `in` keyword to find an element in a list of tuples {#use-in}
Create a for-loop to iterate through the list of tuples. Use the syntax `element in tuple` to check if `tuple` contains `element`, then add the desired tuples to a new list.
```python
tuples = [(1, 2), (3, 4), (2, 4)]
tuples_with_2 = []
for a_tuple in tuples:
  if 2 in a_tuple:
    tuples_with_2.append(a_tuple)
print(tuples_with_2)
```
Use list comprehension for a more compact implementation.
``` python
tuples = [(1, 2), (3, 4), (2, 4)]
print([a_tuple for a_tuple in tuples if 2 in a_tuple])
```
