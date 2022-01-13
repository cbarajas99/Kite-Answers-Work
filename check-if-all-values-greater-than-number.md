headers:
  use-all: Use `all()`
---
# How to check if all values in a list are greater than a certain number in Python
Checking if all values in a list are greater than a certain number results in `True` if each value is larger than the number and `False` if otherwise. For example, checking if the values in `[2, 4, 6]` are greater than `5` results in `False`.

## Use [`all()`](kite-sym:builtins.all) to check if all values in a list are greater than a certain number {#use-all}
Use the generator expression syntax `number > certain_number for number in list_of_numbers` to check if each `number` in `list_of_numbers` is greater than `certain_number`. Call [`all(iterable)`](kite-sym:builtins.all) with the result as `iterable` to return `True` if all values in the list are greater than the certain number and `False` if otherwise.

```python
list_of_numbers = [2, 4, 6]

certain_number = 5
a_boolean = all(number > certain_number for number in list_of_numbers)

print(a_boolean)
```
