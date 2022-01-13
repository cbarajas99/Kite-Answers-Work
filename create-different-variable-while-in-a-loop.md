headers:
  use-string-formatting: Use string formatting
---
# How to create different variables names while in a for-loop in Python
Creating different variables while in a for-loop results in a dictionary containing many different keys mapped to the same value.

## Use string formatting to create different variables names while in a for-loop {#use-string-formatting}
Use a for-loop and ['range(start, stop)'](kite-sym:builtins.range) to iterate over a range from `start` to `stop`. Inside the for-loop, use the string formatting syntax `dict["key%s" % number] = value` to map many different keys in `dict` to the same value `value`.

```python
a_dictionary = {}
for number in range(1,4):
    a_dictionary["key%s" %number] = "abc"

print(a_dictionary)
```
