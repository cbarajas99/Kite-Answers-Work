headers:
  use-str-count: Use `str.count()`
---
# How to count the number of occurrences of a character in a string in Python
The number of occurrences or the count of a character is the number of time it appears in a string. For example, the count of `"a"` in `"aabba"` is 3.

## Use [`str.count()`](kite-sym:builtins.str.count) to count the number of occurrences {#use-str-count}
Call [`str.count(x)`](kite-sym:builtins.str.count) on a string to get the count of `x`.

```python
a_string = "aabba"

# counts the "a" in "aaa"
count = a_string.count("a")

print(count)
```
