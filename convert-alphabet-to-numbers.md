headers:
  use-ord: Use `ord()`
---
# How to convert letters to numbers in Python
Converting letters to numbers results in a list with elements as the result of changing each letters in a string to the number corresponding to its position in the alphabet. For example, changing `"abyz"` to numbers results in `[1, 2, 25, 26]`.

## Use [`ord()`](kite-sym:builtins.ord) to convert letters to numbers {#use-ord}
Use a for-loop to iterate over each letter in a string. At each iteration, [`append`](kite-sym:builtins.append) [`ord(c) - 96`](kite-sym:builtins.ord) with `c` as the current letter to an initially empty list.

```python
letters = "abyz"

numbers = []
for letter in letters:
  number = ord(letter) - 96
  numbers.append(number)

print(numbers)
```
Use a list comprehension for a more compact implementation.
```python
letters = "abyz"

numbers = [ord(letter) - 96 for letter in letters]

print(numbers)
```
