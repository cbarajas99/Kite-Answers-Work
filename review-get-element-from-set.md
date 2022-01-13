headers:
  use-iter-next: Use `iter()` and `next()`

---
# How to get an element from a set in Python
A set is an unordered collection of unique elements. Getting an element from a set returns the value of the element, but does not remove it from the set.

## Use [`iter()`](kite-sym:builtins.iter) and [`next()`](kite-sym:builtins.next) to get an element from a set {#use-iter-next}
Call [`iter(collection)`](kite-sym:builtins.iter) on a set to convert it to an `iterator` object. Call [`next(iterator, default)`](kite-sym:builtins.next) on this iterator with `default` set to `None` to get the next element, or `None` if there are no elements remaining.
```python
a_set = {1, 2}

iterator = iter(a_set)
# gets an item from iterator
item1 = next(iterator, None)
print(item1)

# gets next item from iterator
item2 = next(iterator, None)
print(item2)

item3 = next(iterator, None)
print(item3)
```
> **Warning:**
>  Since sets are unordered, it is not guaranteed that [`next()`](kite-sym:builtins.next) will return the elements in the same order every time.
