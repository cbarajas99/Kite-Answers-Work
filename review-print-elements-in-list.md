headers:
  use-a-for-loop: Use a for-loop
---
# How to print the elements of a list in Python
Printing the elements of a list outputs each element on its own line.

## Use a for-loop to print the elements of a list {#use-a-for-loop}
Use a for-loop to iterate throught the list. At each iteration, call [`print(value)`](kite-sym:builtins.print) with each item as `value` to output the item on its own line.

```python
a_list = ["a", "b", "c"]

for item in a_list:
    # print item on its own line
    print(item)
```
