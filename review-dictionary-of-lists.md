headers:
  create: Create a dictionary of lists
---
# How to create a dictionary of lists in Python
A dictionary of lists is a dictionary whose values are lists. For example, `{"a": [1, 2], "b": [3, 4]}` is a dictionary of lists.

## Use to create a dictionary of lists {#}

```python
a_dictionary = {}
a_list = [[1, 2], [3, 4]]

for number,item in enumerate(a_list):
  a_dictionary[number] = item

print(a_dictionary)
```
