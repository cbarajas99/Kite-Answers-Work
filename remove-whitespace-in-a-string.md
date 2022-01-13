headers:
  use-replace: Use `str.replace()`
  use-strip: Use `str.strip()`
---
# How to remove whitespace from a string in Python
Removing whitespace from a string results in either removing all whitespace or removing leading and ending whitespace from a string.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to remove all whitespace from a string {#use-replace}
Call [`str.replace(old, new)`](kite-sym:string.replace) with `old` as `" "` and `new` as `""` to remove all whitespace from `str`.
```python
a_string = " hello world "

without_all_whitespaces = a_string.replace(" ","")

print(without_all_whitespaces)
```
## Use [`str.strip()`](kite-sym:builtins.str.strip) to remove leading and ending whitespace from a string {#use-strip}
Call [`str.strip()`](kite-sym:builtins.str.strip) to remove leading and ending whitespace from `str`.
```python
a_string = " hello world "

without_leading_and_ending = a_string.strip()

print(without_leading_and_ending)
```
