headers:
  use-isinstance: Use `isinstance()`
---
# How to check if a number is an int or float in Python
Checking if a number is an integer or float evaluates to `True` or `False`. For instance, checking if `25.9` is of type `float` and `int` evaluates to `True` and `False`, respectively.

## Use [`isinstance()`](kite-sym:builtins.isinstance) to check if a number is an int or float {#use-isinstance}
Call [`isinstance(object, classinfo)`](kite-sym:builtins.isinstance) with the number as `object` and `classinfo` as either `int` or `float` to return `True` if `object` is an instance of `classinfo` and `False` otherwise.
```python
number = 25.9

check_int = isinstance(25.9, int)
print(check_int)

check_float = isinstance(25.9, float)
print(check_float)
```
