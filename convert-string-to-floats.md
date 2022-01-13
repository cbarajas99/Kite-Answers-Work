headers:
  use-split: Use `str.split()`
---
# How to convert a string series to a list of floats in Python
Converting a string series to a list of floats results in a list containing each float represented in the string. For example, converting `"1.2 2.3 3.4"` to a list of floats results in `[1.2, 2.3, 3.4]`.

## Use [`str.split()`](kite-sym:builtins.str.split) to convert a string series to a list of floats {#use-split}
Use [`str.split()`](kite-sym:builtins.str.split) to create a list of items separated by whitespace in the string. Create a for-loop to iterate through each item in this list. Use [`float(item)`](kite-sym:builtins.float) to convert each `item` to a float. Call [`list.append(object)`](kite-sym:builtins.list.append) with `object` as the converted float to append it to a new list.

```python
string_series = "1.2 2.3 3.4"

floats_list = []
for item in string_series.split():
  floats_list.append(float(item))

print(floats_list)
```
Use a list comprehension for a more compact implementation.
```python
string_series = "1.2 2.3 3.4"

floats_list = [float(item) for item in string_series.split()]

print(floats_list)
```
