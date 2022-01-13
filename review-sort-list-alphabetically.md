headers:
  use-sorted: Use `sorted()`
---
# How to sort a list alphabetically in Python
In an alphabetically sorted list, items are ordered by the position of their letters in the alphabet. Uppercase letters come before lowercase letters. For instance, sorting `["ab", "b", "B", "aa"]` results in `["B", "aa", "ab", "b"]`.

## Use [`sorted()`](kite-sym:builtins.sorted) to sort a list alphabetically {#use-sorted}
Pass a list into  [`sorted(iterable)`](kite-sym:builtins.sorted) to sort it alphabetically.
```python
# takes capitalization into consideration
sorted_list = sorted(["ab", "b", "B", "aa"])

print(sorted_list)
```
[`sorted(iterable, key=None)`](kite-sym:builtins.sorted) takes an optional key that specifies how to sort. To disregard capitalization when sorting a list, set `key` to [`str.lower`](kite-sym:builtins.str.lower).

```python
# disregards capitalization
sorted_list = sorted(["ab", "b", "B", "aa"], key=str.lower)

print(sorted_list)
```
