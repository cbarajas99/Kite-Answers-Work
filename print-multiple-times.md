headers:
  use-range: Use `range()`
---
# How to print a string multiple times in Python
Printing a string multiple times will return multiple lines of a string where each line contains a string multiple times.

## Use [`range()`](kite-sym:builtins.range) to print a string multiple times {#use-range}
Use [`range(stop)`](kite-sym:builtins.range) to create a range of `0` to `stop` where  `stop` is the number of lines desired. Use a for-loop to iterate through this range. In each iteration, concatenate the string to itself by the number of times desired and print the result.

```python
a_string = "abc"
for line in range(3):
  result = a_string * 2
  print(result)
```
