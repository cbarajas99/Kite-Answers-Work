headers:
  use-any: Use `any()`
---
# How to check if a list contains a substring in Python
A list contains a substring if any item in the list contains that substring. For example, `["one", "two", "three"]` contains `wo` because `wo` is a substring of `two`.

## Use [`any()`](kite-sym:builtins.any) to check if a list contains a substring {#use-any}
Call [`any(iterable)`](kite-sym:builtins.any) with `iterable` as a for-loop that checks if any element in the list contains the substring.
```python
strings = ["one", "two", "three"]
substring = "wo"

# results in boolean
substring_in_list = any(substring in string for string in strings)

print(substring_in_list)
```
Alternatively, use a list comprehension to construct a new list containing each element that contains the substring.
```python
strings = ["one", "two", "three"]
substring = "wo"

# list of items that contain substring
strings_with_substring = [string for string in strings if substring in string]

print(strings_with_substring)
```
> **Further reading:**
> List comprehensions provide a concise way to create lists. Read more about list comprehensions [here](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions).
