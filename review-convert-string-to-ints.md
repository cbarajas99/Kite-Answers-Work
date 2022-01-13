headers:
  use-map: Use `map()`
---
# How to convert a list of strings to ints in Python
Converting a list of strings to ints converts each string in the list into an integer. For example, converting `["1", "2", "3"]` returns `[1, 2, 3]`.

## Use [`map()`](kite-sym:builtins.map) to convert a list of strings to ints {#use-map}

Use [`map(function, iterable)`](kite-sym:builtins.map) with a list of strings as `iterable` and `int` as `function` to apply [`int()`](kite-sym:builtins.int) to each string in the list. Use [`list(iterable)`](kite-sym:builtins.list) with the output of `map()` as `iterable` to convert to a list.

```python
string_list = ["1", "2", "3"]

# maps each string to an int
integer_map = map(int, string_list)
# converts mapped output to a list of ints
integer_list = list(integer_map)

print(integer_list)
```
