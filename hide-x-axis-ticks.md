headers:
  use-tickparams: Use `matplotlib.pyplot.tick_params()`
---
# How to remove the x-axis ticks from a Matplotlib graph in Python
Removing the x-axis ticks from a graph results in a graph whose x-axes has labels but no ticks.

## Use [`matplotlib.pyplot.tick_params()`](kite-sym:matplotlib.pyplot.tick_params) to remove the x-axis ticks from a Matplotlib graph {#use-tickparams}
Call [`matplotlib.pyplot.tick_params(axis = None, which = None, bottom = None, top = None)`](kite-sym:matplotlib.pyplot.tick_params) with `axis` set to `"x"`, `which` set to `"both"`, `bottom` set to `False`, and `top` set to `False`.

```python
KITE.start_prelude()
import matplotlib.pyplot as plt
KITE.stop_prelude()

plt.plot(range(10))
plt.tick_params(axis = "x", which = "both", bottom = False, top = False)

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```

> **Further reading:**
> [`matplotlib.pyplot.tick_params()`](kite-sym:matplotlib.pyplot.tick_params) has additional arguments that can be used to change the appearance of the ticks and tick labels of a graph. Read more about the arguments of [`pyplot.tick_params()`](kite-sym:matplotlib.pyplot.tick_params) [here](https://kite.com/python/docs/matplotlib.pyplot.tick_params).
