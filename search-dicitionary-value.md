headers:
  use-values: Use `dict.values()``
---
# How to search if dictionary value contains certain string in Python
Searching if a certain string is in a dictionary value, where the values are a list of strings, results in a list printing the values containing that string.

## Use [`dict.values()`](kite-sym:builtins.dict.values) to search if dictionary value contains certain string {#iterate-values}
Use [`dict.values()`](kite-sym:builtins.dict.values) to get a list of the values in the dictionary. Create a for-loop to iterate this list of values. Use an if-statement to check if the certain string is in the values.

```python
a_dict = { "a" : ["1", "3"], "b" : ["3","4"], "c": ["5", "6"]}

search = "3"
values = []
for value in a_dict.values():
  if search in value:
        values.append(value)

print(values)
```
Use list comprehension for a more compact implementation.
```python
a_dict = { "a" : ["1", "3"], "b" : ["3","4"], "c": ["5", "6"]}

search = "3"
values = [value for value in a_dict.values() if search in value]

print(values)
```
