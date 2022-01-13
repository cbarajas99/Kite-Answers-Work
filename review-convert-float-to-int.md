headers:
  use-int: Use `int()`
---
# How to convert a float to an integer in Python
Converting a float to an integer changes the float to the nearest smaller whole number. For example, converting `1.1` to an integer results in `1`.

## Use [`int()`](kite-sym:builtins.int) to convert a float to an integer {#use-int}
Call  [`int(x)`](kite-sym:builtins.int) with a float as `x` to change it to an integer.
```python
a_float = 1.1

#floats truncate to zero
a_integer = int(1.1)

print(a_integer)
```
