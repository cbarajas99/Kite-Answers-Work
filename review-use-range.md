headers:
  range: Use `range()`
---
# How to use `range()` in Python
The built-in [`range()`](kite-sym:builtins.range) function is used to generate immutable sequences of integers.

## Use [`range()`](kite-sym:builtins.range) to generate an immutable sequence of integers {#range}
Call [`range(stop)`](kite-sym:builtins.range) and specify `stop` to return a sequence of integers from `0` up to `stop`.
```python
# range of numbers from 0 to 3
a_range = range(4)
for number in a_range:
  print(number)
```

Call [`range(start, stop)`](kite-sym:builtins.range) and specify both `start` and `stop` to return a sequence of integers from `start` up to `stop`.
```python
# range of numbers from 1 to 3
a_range = range(1, 4)
for number in a_range:
  print(number)
```

Call [`range(start, stop, step)`](kite-sym:builtins.range) and specify `start`, `stop`, and `step` to return a sequence of integers from `start` up to `stop` incremented by `step`.
```python
a_range = range(1, 4, 2)
for number in a_range:
  print(number)
```
