headers:
  use-print: Use `print()`
---
# How to suppress the newline after a print statement in Python
Suppressing the newline after a print statement goes through a list and print all the items in the same line. For example, supressing the newline after a print statement in `["this will", "all be printed", "on one line"]` results in `this will all be printed on one line`.

## Use [`print()`](kite-sym:builtins.print) to suppress the newline after a print statement {#use-print}
Use a for-loop to iterate through the list. At each iteration, call [`print(item, end)`](kite-sym:builtins.print) with `item` as the item in the list and `end` as `end=" "` to suppress the newline after the print statement.
```python
a_list = ["this will", "all be printed", "on one line"]

for item in a_list:
  print(item, end=" ")
```
