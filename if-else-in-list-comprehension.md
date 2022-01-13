headers:
  place-before-for: Place before the first for statement
---
# How to use if-else variants in list comprehensions in Python
Using if-else variants in a list comprehension constructs a list of values according to a certain condition. For example, constructing a list using the if-else variant `x if x % 3 == 0 else x % 3` results in `[1, 2, 3, 1, 2, 6, 1, 2, 9]`.

## Place an if-else variant before the for statement in list comprehensions {#place-before-for}
Place the if-else variant before the first for-statement in the list comprehension.
```python
a_list = [x if x % 3 == 0 else x % 3 for x in range(1,10)]

print(a_list)
```
If using only an if-statement, place the if-statement after the last for-statement.

```python
a_list = [x for x in range(1, 10) if x % 3 == 0]

print(a_list)
```
