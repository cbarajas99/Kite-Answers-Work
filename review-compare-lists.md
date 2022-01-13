headers:
  use-set-intersection: Use `set.intersection()`
---
# How to compare common elements in two lists in Python
Comparing two lists results in the common elements between them. For example, `2` and `3` are common elements of `[1, 2, 3]` and `[2, 3, 4]`.

## Use [`set.intersection()`](kite-sym:builtins.set.intersection) to compare two lists and return the common elements {#use-set-intersection}
Call `set(*args)` with one of the lists as `*args` to convert it to a set. With this new set, call `set.intersection(*s)` to return a set containing the common elements between `set` and the list `*s`.

```python
list1 = [1, 2, 3]
list2 = [2, 3, 4]

set1 = set(list1)
# set containing common elements
common_elements = set1.intersection(list2)

print(common_elements)
```

>**Further Reading:**
> There are many ways to compare two lists. See more information on comparing the distance metrics of two lists [here] (https://docs.scipy.org/doc/scipy/reference/spatial.distance.html).
