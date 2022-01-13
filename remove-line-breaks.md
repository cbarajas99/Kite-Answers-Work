headers:
  use-replace: Use `str.replace()`
---
# How to remove all line breaks from a string
Removing all line breaks from a string results in the string being displayed in one line.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to remove all line breaks from a string {#use-replace}
Call [`str.replace(old, new)`](kite-sym:builtins.str.replace) where `old` is `"\n"` and `new` is `" "` to replace the line breaks with a single space.
```python
a_string = """abc
def
ghi"""
print(a_string)

without_line_breaks = a_string.replace("\n", " ")

print(without_line_breaks)
```
