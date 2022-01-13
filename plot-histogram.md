headers:
  use-hist: Use `matplotlib.pyplot.hist()`
---
# How to plot a histogram in Matplotlib in Python
Plotting a histogram in [`Matplotlib`](kite-sym:matplotlib) displays a histogram with labeled axes.

## Use [`matplotlib.pyplot.hist`](kite-sym:matplotlib.pyplot.hist) to plot a histogram in Matplotlib {#use-hist}
Call [`matplotlib.pyplot.hist(x, bins=n)`](kite-sym:matplotlib.pyplot.hist) to plot a histogram of an array of data `x` with `n` bars. Call [`matplotlib.pyplot.xlabel(xlabel)`](kite-sym:matplotlib.pyplot.xlabel) or [`matplotlib.pyplot.ylabel(ylabel)`](kite-sym:matplotlib.pyplot.ylabel) to label the x-axis `xlabel` or y-axis `ylabel` respectively.

```python
KITE.start_prelude()
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(10)
KITE.stop_prelude()

#generate random array
data = np.random.normal(size = 1000)

plt.hist(data, bins = 20)
plt.xlabel('Data')
plt.ylabel('Frequency')

KITE.set_display_code(False)
plt.savefig("sample_histogram.jpg")
KITE.display_image("sample_histogram.jpg")
KITE.set_display_code(True)
```
