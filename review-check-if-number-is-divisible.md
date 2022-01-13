headers:
  use-mod: Use the modulus operator
---
# How to check if a number is divisible by another number in Python
A number is divisible by another number if division between them does not result in a remainder.

## Use the modulus operator to check if a number is divisible by another number {#use-mod}
Use the modulus operator `%` to get the remainder from dividing a number by another number. Use the comparison operator `==` to compare the remainder with `0`. This returns `True` if the number is divisible, or `False` otherwise.

```python
remainder = 10 % 2

# checks if 10 is divisible by 2
is_divisible = remainder == 0

print(is_divisible)
```
```python
remainder = 10 % 3

# checks if 10 is divisible by 3
is_divisible = remainder == 0

print(is_divisible)
```
