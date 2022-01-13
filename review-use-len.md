headers:
  use-len: Use `len()`
---
# How to use `len()` in Python
The builtin [`len(obj)`](kite-sym:builtins.len) function is used to find the lengths of objects by calling their own length methods. For example, using [`len(obj)`](kite-sym:builtins.len) on a string calls the [`str.__len__()`](kite-sym:builtins.str) method to find the length of the string.

## Use [`len()`](kite-sym:builtins.len) to find the length of an object {#use-len}
Use [`len(obj)`](kite-sym:builtins.len) on `obj` to find its length. `obj` may be a sequence (e.g. a string, tuple, or list) or a mapping (e.g. a dictionary).
```python
a_string = "abc"

#results in length of string
string_length = len(a_string)

print(string_length)
```
```python
a_list = [1, 2, 3]

#results in length of list
list_length = len(a_list)

print(list_length)
```
```python
a_dict = {"a": 1, "b": 2}

#results in length of dictionary
dictionary_length = len(a_dict)

print(dictionary_length)
```
