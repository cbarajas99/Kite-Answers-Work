headers:
  use-colormap: Use a colormap
---
# How to use a colormap to set the color of lines in a Matplotlib line graph in Python
Setting the line color in a line graph results in a line graph where each line color is specified by a colormap.

## Use a colormap to set the color of a line in a Matplotbib line graph {#use-colormaps}
Call [`numpy.linspace(start, stop, num)`](kite-sym:numpy.linspace) to create an evenly spaced interval with `start` as `0`, `stop` as `1`, and `num` as the length of the list containing all the lines to be plotted. Use list-comprehension to create a list of colors, and call [`matplotlib.cm.rainbow(array)`](kite-sym:matplotlib.cm.rainbow) where `array` is each element in the evenly spaced interval. Use a for-loop to iterate through [`enumerate(iterable)`](kite-sym:builtins.enumerate) with `iterable` as the list of colors. Call [`matplotlib.pyplot.plot(i, color)`](kite-sym:matplotlib.pyplot.plot) with `i` as the i-th element in the list containing lines.

```python
KITE.start_prelude()
import matplotlib.pyplot as plt
import matplotlib.cm as cm
import numpy as np
KITE.stop_prelude()

x = np.linspace(0, 10, 100)
lines = [np.sin(x), np.cos(x), np.sin(x + 5)]

evenly_spaced_interval = np.linspace(0, 1, len(lines))
colors = [cm.rainbow(x) for x in evenly_spaced_interval]
for i, color in enumerate(colors):
    plt.plot(lines[i], color = color)

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
