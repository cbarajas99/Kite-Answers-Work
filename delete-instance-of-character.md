headers:
  use-replace: Use `str.replace()`
---
# How to delete all instances of a character in a string in Python
Deleting all instances of a character in a string modifies the string to not contain a specified character. For example, deleting all instances of `"e"` in `"replace all e's"` results in `"rplac all 's"`.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to delete all instances of a character in a string {#use-replace}
Call [`str.replace(old, new)`](kite-sym:builtins.str.replace) with `old` as the character that is going to be deleted and with `new` as `""`.
```python
a_string = "replace all e's"

string_without_e = a_string.replace("e","")

print(string_without_e)
```
> **Further Reading:**
> There are more ways to replace characters within a string with [`str.replace()`](kite-sym:builtins.str.replace), read [here](kite-sym:builtins.str.replace) to learn more.
