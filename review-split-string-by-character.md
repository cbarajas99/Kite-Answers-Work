headers:
  use-split: Use `str.split()`
---
# How to parse a string in Python
Parsing a string splits the string into substrings by a specified delimeter. For example, parsing `"ab_cd_ef"` by t `"_"` results in `["ab","cd","ef"]`.

## Use [`str.split()`](kite-sym:builtins.str.split) to split the string {#use-split}
Call [`str.split(sep)`](kite-sym:builtins.str.split) to parse the string `str` by the delimeter `sep` into a list of strings.
```python
original_string = "ab_cd_ef"

# splits string by "_"
split_string = original_string.split("_")

print(split_string)
```

Call [`str.split(sep, maxsplit)`](kite-sym:builtins.str.split) and state the `maxsplit` parameter to specify the maximum number of splits to perform.  These splits are executed from the left hand side.
```python
a_string = "ab_cd_ef"

# splits string by the first "_"
parsed_string = a_string.split("_", 1)

print(parsed_string)
```
