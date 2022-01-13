headers:
  use-str-split: Use `str.split()`
---
# How to split a string by a character in Python
Splitting a string results in a list of the substrings between a specific character or other delimiter. For example, splitting `"a-b-c"` by `"-"` results in `["a", "b", "c"]`.

## Use [`str.split()`](kite-sym:builtins.str.split) to split a string by a character {#use-str-split}
Call [`str.split(sep)`](kite-sym:builtins.str.split) to split `str` by `sep`.

```python
a_string = "a-b-c"

# split a_string by "-"
separated_strings = a_string.split("-")

print(separated_strings)
```
