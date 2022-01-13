headers:
  use-range: Use `range()`
---
# How to split a string at every nth character in Python
Splitting a string at every nth character returns a list of strings that are of length n, but for the last split string in the list `0 < len(last_string) <= n` because the entire string does not need to be of multiple of n.

## Use [`range()`](kite-sym:builtins.range) to split a string at every nth character {#use-range}
Use a for-loop and [`range(start, stop, step)`](kite-sym:builtins.range) to iterate over a range from `start` to `stop` where `stop` is the [`len(string)`](kite-sym:builtins.len) and `step` is every number of characters where the string will be split. Use string slicing syntax `string[index : index + step]` to acquire a string with `step` characters. Use [`list.append()`](kite-sym:builtins.list.append) to add that previously described string to a list.

```python
a_string = "abcde"

split_strings = []
n  = 2
for index in range(0, len(a_string), n):
    split_strings.append(a_string[index : index + n])

print(split_strings)
```
Use list comprehension for a more compact implementation
```python
a_string = "abcde"

a_list = []
n = 2
split_strings = [a_string[index : index + n] for index in range(0, len(a_string), n)]

print(split_strings)
```
