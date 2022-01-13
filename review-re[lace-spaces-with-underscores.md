headers:
  use-replace: Use `replace()`
---
# How to replace spaces with underscores in Python
Replacing spaces with underscores changes every occurrence of `" "` to `"_"`. For example, replacing the spaces in `"a b c"` results in `"a_b_c"`

## Use [`str.replace()`](kite-sym:builtins.str.replace) to replace spaces with underscores {#use-replace}
Call [`str.replace(old, new)`](kite-sym:builtins.str.replace) with a space as `old` and an underscore as `new` to replace all spaces with underscores in a string.
```python
a_string = "a b c"

# replaces spaces with `"_"`
new_string = a_string.replace(" ", "_")

print(new_string)
```
