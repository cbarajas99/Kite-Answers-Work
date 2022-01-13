headers:
  use-for-loop: Use a for-loop
---
# How to convert all items in a list to floats in Python
Converting all items in a list to floats converts every item in the list from type `str` or type `int` to type `float`. For instance, converting `["1.2", "3.4", "5.6"]` to a list of floats results in `[1.2, 3.4, 5.6]`.

## Use a for-loop to convert all items in a list to floats {#use-for-loop}
Use a for-loop and the syntax `item in list` to iterate throughout `list`. Use [`float(x)`](kite-sym:builtins.float) with `item` as `x` to convert `item` to type `float`. Append the converted `item` to a new list.
```python
a_list = ["1.2", "3.4", "5.6"]

list_of_floats = []
for item in a_list:
    list_of_floats.append(float(item))

print(list_of_floats)
```
Use a list comprehension for a more compact implementation.
```python
a_list = ["1.2", "3.4", "5.6"]

list_of_floats = [float(item) for item in a_list]

print(list_of_floats)
```
> **Further reading:**
> List comprehensions provide a concise way to create lists. Read more about list comprehensions [here](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions).
