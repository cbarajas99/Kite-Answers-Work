headers:
  zips: Use `zip()`
---
# How to find the sum of two lists in Python
Adding two lists results in a new list where each element is the sum of the elements in the corresponding positions of the two lists. For example, `[1, 2, 3]` + `[4, 5, 6]` = `[5, 7, 9]`.

## Use [`zip()`](kite-sym:builtins.zip) to find the sum of two lists {#zips}
Call [`zip(iter1, iter2)`](kite-sym:builtins.zip) with one list as `iter1` and another as `iter2` to generate a zip object containing pairs of corresponding elements from both lists. Use a list comprehension to create a new list where each element is the sum of each pair.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

# zipped_lists contains pairs of items from both lists
zipped_lists = zip(list1, list2)
sum = [x + y for (x, y) in zipped_lists]

print(sum)
```
