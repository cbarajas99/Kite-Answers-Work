headers:
  use-map: Use `map()`
---
# How to convert a list of booleans to ints in Python
Converting a list of booleans to ints converts each boolean in the list into an integer. `True` converts to `1`, and `False` converts to `0`. For example, converting `[True, False]` returns `[1, 0]`.

## Use [`map()`](kite-sym:builtins.map) to convert a list of booleans to ints {#use-map}
Use [`map(function, iterable)`](kite-sym:builtins.map) with a list of booleans as `iterable` and `int` as `function` to apply [`int()`](kite-sym:builtins.int) to each boolean in the list. Use [`list(iterable)`](kite-sym:builtins.list) with the output of `map()` as `iterable` to convert to a list.

```python
boolean_list = [True, False]

# maps each boolean to an int
integer_map = map(int, boolean_list)
# converts mapped output to a list
integer_list = list(integer_map)

print(integer_list)
```
