headers:
  use-comparison-operators: Use the comparison operators
  use-in: Use the `in` keyword
---
# How to check if a number is between two numbers in Python
Checking if a number is between two numbers returns `True` if the number is greater than or equal to the minimum of the two numbers and less than or equal to the maximum. For example, checking if `13` is between `5` and `10` returns `False`.

## Use the comparison operators to check if a number is between two numbers {#use-comparison-operators}
Use the syntax `minimum <= number <= maximum` such that `maximum` is greater than `minimum` to return True if `number` is between `minimum` and `maximum` and `False` if otherwise.

```python
is_between = 5 <= 13 <= 10
print(is_between)
```
## Use the `in` keyword to check if an integer is between two integers {#use-in}
Call [`range(start, stop)`](kite-sym:builtins.range) to create a range of integers from `start` up to `stop`. Use the `in` keyword to check if an integer is in this range.

```python
a_range = range(5, 11)
is_between = 13 in range(5, 11)
print(is_between)
```
