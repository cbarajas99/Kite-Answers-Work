headers:
  use-less-than: Use the `<` operator

---
# How to check if a value is less than another value in Python

Checking if a value is less than another value returns `True` if the former is less than the latter and `False` if otherwise. For example, `1 < 2` returns `True`.

## Use the `<` operator to check if a value is greater than another value {#use-less-than}
Insert the less-than operator `<` in between two values to create a boolean expression that returns `True` if the left value is less than the right value and `False` if otherwise.

```python
# results in boolean
is_less_than = 1 < 2

print(is_less_than)
```
```python
# results in boolean
is_less_than = 2 < 1

print(is_less_than)
```
```python
# results in boolean
is_less_than = 1 < 1

print(is_less_than)
```
