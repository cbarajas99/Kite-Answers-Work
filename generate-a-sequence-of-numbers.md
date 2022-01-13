headers:
  use-range: Use `range()`
---
# How to generate a sequence of numbers in Python
Generating a sequence of numbers results in a list of numbers within a range that each satisfy a certain requirement. For instance, the numbers between `1` and `10` that have a remainder of `1` or `2` when divided by `5` are `[1, 2, 5, 7]`.

## Use [`range()`](kite-sym:builtins.range) to generate a sequence of numbers {#use-range}
Call [`range(start, stop)`](kite-sym:builtins.range) to generate a sequence of numbers from `start` up to `stop`. Use a for-loop to iterate over each number in this sequence and use [`list.append(x)`](kite-sym:builtins.list.append) to append the number to an empty list if it meets a certain condition.
```python
numbers = range(1, 10)

sequence_of_numbers = []
for number in numbers:
   if number % 5 in (1, 2):
      sequence_of_numbers.append(number)

print(sequence_of_numbers)
```
Use a list comprehension for a more compact implementation.
```python
numbers = range(1, 10)

sequence_of_numbers = [number for number in numbers if (number % 5 in (1, 2))]

print(sequence_of_numbers)
```
