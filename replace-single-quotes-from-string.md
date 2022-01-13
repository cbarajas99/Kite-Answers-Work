headers:
  use-replace: Use `str.replace()`
---
# How to remove single quotes from a string in Python
Removing single quotes from a string results in a modified string that does not contain single quotes. For example, removing single quotes from `"He said 'Hello' to me"` results in `"He said Hello to me"`.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to remove single quotes from a string {#use-replace}
Call [`str.replace(old, new)`](kite-sym:builtins.str.replace) with `old` as `"'"` and `new` as `""` to remove all single quotes from the string.  
```python
original_string = "He said 'Hello' to me"

new_string = original_string.replace("'", "")

print(new_string)
```
