headers:
  use-groupby: Use `panda.DataFrame.groupby()`
---
# How to color a scatter plot by category using Matplotlib in Python
Coloring a scatter plot by category using [Matplotlib](kite-sym:matplotlib) displays a scatter plot with different color data points for each category.

## Use [`panda.DataFrame.groupby()`](kite-sym:pandas.core.generic.NDFrame.groupby) to plot by category in Matplotlib {#use-groupby}
Call [`pandas.DataFrame(data)`](kite-sym:pandas.DataFrame) with `data` as `{"a": x, "b": y, "c":z}` with `x`, `y`, and `z` as arrays of x-values, y-values and category labels for each data point, respectively, to create a [`DataFrame`](kite-sym:pandas.DataFrame) with column names `"a"`, `"b"`, and `"c"`. Call [`pandas.DataFrame.groupby(by)`](kite-sym:pandas.core.generic.NDFrame.groupby) with `pandas.DataFrame` as the previous result and `by` as the name of the labels column to group `pandas.DataFrame` by `by`. Use the syntax `for name, group in groups` to iterate through the previous result `groups`.  At each iteration, call [`matplotlib.pyplot.plot(scalex, scaley, marker="o", linestyle="", label=name)`](kite-sym:matplotlib.pyplot.plot) with `scalex` and `scaley` as the x and y-data columns of `group` to plot each group separately. Call [`matplotlib.axes.Axes.legend()`](kite-sym:matplotlib.axes.Axes.legend) to place a legend on the axes.

```python
KITE.start_prelude()
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
np.random.seed(0)
number_of_points = 10
x, y = np.random.random((2, number_of_points))
x = x * 10 + 1
y = y * 10 + 1
x = x.astype(int)
y = y.astype(int)
labels = np.random.choice(['1', '2', '3'], number_of_points)
KITE.stop_prelude()

# x, y, and labels are pre-existing arrays
data = pd.DataFrame({"X Values": x, "Y Values": y, "Category": labels})
print(data)
groups = data.groupby("Category")

for name, group in groups:
    plt.plot(group["X Values"], group["Y Values"], marker="o", linestyle="", label=name)
plt.legend()

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
