headers:
  use-rainbow: Use `matplotlib.cm.rainbow()`
---
# How to set different colors for each series in a Matplotbib scatter plot in Python
Setting different colors for each series in a scatter plot results in different colors being used for each of the series of x and y coordinates.

## Use [`matplotlib.cm.rainbow()`](kite-sym:matplotlib.cm.rainbow) to set different colors for each series in a Matplotlib scatter plot {#use-rainbow}
Call [`matplotlib.cm.rainbow(array)`](kite-sym:matplotlib.cm.rainbow) where `array` is [`numpy.linspace(start, stop, num)`](kite-sym:numpy.linspace) with `start` as `0`, `stop` as `1`, and `num` as the length of the list containing arrays of the y-coordinates to create a list of numbers that represent colors. Call [`iter(iterable)`](kite-sym:builtins.iter) with `iterable` as the list of colors. Loop over the y-coordinates and for each coordinate `y`, call [`matplotlib.pyplot.scatter(x, y, color)`](kite-sym:matplotlib.pyplot.scatter) with `x` as the array of x-coordinates and `color` as [`next(iterator)`](kite-sym:builtins.next) with `iterator` as the list of colors.
```python
KITE.start_prelude()
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.cm as cm
import random
random.seed(10)
x_coordinates = np.arange(5)
y_coordinates = [(random.randint(0,10) * x_coordinates + i) for i in range(5)]

for i in range(5):
    print("Data Series " + str(i) +": " + ", ".join(map(str, zip(x_coordinates, y_coordinates[i]))))
KITE.stop_prelude()

colors = iter(cm.rainbow(np.linspace(0, 1, len(x_coordinates))))
for y in y_coordinates:
    plt.scatter(x_coordinates, y, color=next(colors))

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
