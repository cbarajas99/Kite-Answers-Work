headers:
  use-del: Use `del`
---
# How to remove the last element from a list in Python
Removing the last element of a list shortens the list to exclude the final element. For example, removing the last element from `[1, 2, 3]` results in `[1, 2]`.

## Use the `del` keyword {#use-del}
Use the `del` keyword and the slicing notation `list[-1]` to remove the last element from a list.

```python
a_list = [1, 2, 3]

# deletes the last element
del a_list[-1]

print(a_list)
```
**Further reading:**
Lists support a slicing syntax to access its elements. You can read more about list slicing [here](https://docs.python.org/3/tutorial/introduction.html#lists).
