headers:
  use-print: Use `print()`
---
# How to print in one line in Python
By default, printing an item also prints a newline character after the item is printed. Printing in one line prints the item without a newline character.

## Use [`print()`](kite-sym:builtins.print) to print in one line {#use-print}
Call [`print(item, end)`](kite-sym:builtins.print) with `end` as `end = " "`to print `item` followed by a space instead of a newline.

```python
a_list = [1, 2, 3]

for item in a_list:
    # each print statement followed by a space
    print(item, end = " ")
```
