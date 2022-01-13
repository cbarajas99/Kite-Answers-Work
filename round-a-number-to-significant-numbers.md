headers:
  use-round: Use `round()`
---
# How to round a number to significant digits in Python
Rounding a number to n significant digits rounds a number and includes only the desired number of significant digits

## Use [`round()`](kite-sym:builtins.round) to round a number to significant digits {#use-round}
Use [`round(number, ndigits)`](kite-sym:builtins.round) with `number` as the number being rounded. `ndigits` is the number of significant digits - (int(math.floor(math.log10(abs(`number`)))) - 1).

```python
KITE.start_prelude()
import math
KITE.stop_prelude()

a_number = 123.45
significant_digits = 4
rounded_number =  round(a_number, significant_digits - int(math.floor(math.log10(abs(a_number)))) - 1)

print(rounded_number)
```
