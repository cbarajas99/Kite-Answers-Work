headers:
  slice: Slice the string
---
# How to get the first few characters of a string in Python
Getting the first few characters of a string results in a new string excluding the remaining characters. For example, getting the first two characters of `"abc"` results in `"ab"`.

## Slice the string to get the first few characters {#slice}
Use the slicing syntax `string[:x]` to get the first `x` characters of `string`.
```python
a_string = "abc"

# gets the first two characters
first_2 = a_string[:2]

print(first_2)
```

> **Further reading:**
> Strings support a slicing syntax to access their characters. Read more about string slicing [here](https://docs.python.org/3/tutorial/introduction.html#strings).
