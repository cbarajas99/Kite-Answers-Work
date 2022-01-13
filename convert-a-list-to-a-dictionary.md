headers:
  use-in: Use the `in` keyword
---
# How to convert a list to a dictionary in Python
Converting a list to a dictionary results in a dictionary where the keys and values are taken from the even and odd positions of the list, respectively.

## Use the `in` keyword to convert a list to a dictionary in Python {#use-in}
Use a for-loop and [ `range(start, stop, step)`](kite-sym:builtins.range) to iterate over a range from `start` to `stop` where `stop` is [`len(list)`](kite-sym:builtins.len) and `step` is `2`. Map each key to a value in the dictionary where each key is an even indexed element and each value is the following odd indexed element.

```python
a_list = ["a", 1, "b", 2, "c", 3]

a_dictionary = {}
for index in range(0, len(a_list), 2):
  a_dictionary[a_list[index]] = a_list[index + 1]

print(a_dictionary)  
```
Use a dictionary comprehension for a more compact implementation.
```python
a_list = ["a", 1, "b", 2, "c", 3]

a_dictionary = {a_list[index] : a_list[index + 1] for index in range(0, len(a_list), 2)}

print(a_dictionary)
```
