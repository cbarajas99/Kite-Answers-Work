headers:
  use-for: Use a for-loop
---
# How to print items in a list on separate lines in Python
Printing items in a list results in each item being printed on separate lines.

## Use a for-loop to print items in a list on separate lines {#use-for}
Create a for-loop to iterate through the items of the list. At each iteration, call [`print(item)`](kite-sym:builtins.print) to print each `item`.
```python
a_list = ["this", "will be", "printed on separate", "lines"]

for item in a_list:
  print(item)
```
