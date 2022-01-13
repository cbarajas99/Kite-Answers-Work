headers:
  use-product: Use `itertools.product()`
---
# How to make a combination of a list of lists in Python
Making a combination of a list of lists results in a list of all lists where the `n`th element of each list is an element of the `n`th original list. This is also known as the Cartesian product of the lists. For example, `[[1, 2], [3, 4]]` results in `[(1, 3), (1, 4), (2, 3), (2, 4)]`.

## Use  [`itertools.product()`](kite-sym:itertools.product) to make a combination of a list of lists {#use-product}
Call [`itertools.product(*args)`](kite-sym:itertools.product) with `args` as the list of lists. Use [`list(object)`](kite-sym:builtins.list) to convert the product `object` into a list.

```python
KITE.start_prelude()
import itertools
KITE.stop_prelude()

list_of_lists = [[1,2],[3,4]]

products = itertools.product(*list_of_lists)
products_list = list(products)

print(products_list)
```
