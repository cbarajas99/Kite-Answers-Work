headers:
  use-symmetric-difference: Use `set.symmetric_difference()`
---
# How to get the difference between two strings in Python
Getting the difference between two strings results in a set that contains the characters that are in either string but not both. For instance, the difference between `"abc"` and `"cdef"` results in `{'a', 'b', 'd', 'f', 'e'}`.

## Use [`set.symmetric_difference()`](kite-sym:builtins.set.symmetric_difference) to get the difference between two strings {#use-symmetric-difference}
Call [`set(string)`](kite-sym:builtins.set) to convert `string` into a set. Repeat with the other string to convert it into a set. Call [`first_set.symmetric_difference(second_set)`](kite-sym:builtins.set.symmetric_difference) to return the difference between `first_set` and `second_set`.
```python
string1 = "abc"
string2 = "cdef"

first_set = set(string1)
second_set = set(string2)
difference = first_set.symmetric_difference(second_set)

print(difference)
```
