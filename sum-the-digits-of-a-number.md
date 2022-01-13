headers:
  use-in: Use the `in` keyword
---
# How to sum the digits of a number in Python
The sum of the digits of a number means adding up each of the digits and returning the sum. For instance, the sum of the digits of `123` is `6`.

## Use the `in` keyword {#use-in}
Use [`str()`](kite-sym.builtins.str) to convert the number to a string. Create a for-loop to iterate through this string. Use [`int()`](kite-sym:builtins.int) to convert the string digit to an integer. Add this digit to the sum of the digits in each iteration.
```python
number = 123

sum_of_digits = 0
# turn to string to iterate through
for digit in str(number):
  sum_of_digits += int(digit)

print(sum_of_digits)

```  
Use [`sum()`](kite-sym.builtins.sum) for a more compact implementation.
```python
number = 123

sum_of_digits = sum(int(digit) for digit in str(number))

print(sum_of_digits)
```
