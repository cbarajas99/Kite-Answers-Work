headers:
  single-whitespace: Print a single whitespace
  multiple-whitespaces: Print multiple whitespaces
---
# How to print spaces in Python
Printing spaces results in empty spaces being displayed.

## Print a single whitespace {#single-whitespace}
 Call [`print(value)`](kite-sym:builtins.print) with value as `" "` to print a space on a single line.
```python
print(" ")
```

## Print multiple whitespaces {#multiple-whitespaces}
Call [`print(value)`](kite-sym:builtins.print) with value as `" "*n` to print `n`-many spaces on a single line.
```python
n = 5

print(" " * n)
```
