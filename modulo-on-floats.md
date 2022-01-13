headers:
  use-fmod: Use `math.fmod()`
---
# How to calculate modulo on a float in Python
Given two positive floats `x` and `y`, `x` modulo `y` is equal to the remainder of `x` wholly divided by `y`. For instance, `10.5` modulo `3.25` is `0.75`.

## Use [`math.fmod()`](kite-sym:math.fmod) to calculate modulo on a float point number {#use-fmod}
Call [`math.fmod(x, y)`](kite-sym:math.fmod) to return `x` modulo `y`.
```python
KITE.start_prelude()
import math
KITE.stop_prelude()

x = 10.5
y = 3.25

float_modulo = math.fmod(x, y)

print(float_modulo)
```
