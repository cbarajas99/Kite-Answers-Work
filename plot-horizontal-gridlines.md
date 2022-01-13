headers:
  use-ygrid: Use `matplotlib.axis.YAxis.grid()`
  use-grid: Use `matplotlib.pyplot.grid()`
---
# How to plot horizontal gridlines in a Matplotlib graph in Python
Plotting horizontal gridlines results in a [`Matplotlib`](kite-sym:matplotlib) graph with horizontal gridlines.

## Use [`matplotlib.axis.YAxis.grid()`](kite-sym:matplotlib.axis.YAxis.grid) to only plot horizontal gridlines in a graph {#use-ygrid}
Use [`matplotlib.pyplot.gca()`](kite-sym:matplotlib.pyplot.gca) to get the current axes of the graph. Call [`matplotlib.axis.yaxis.grid()`](kite-sym:matplotlib.axis.YAxis.grid) on the previous axes to plot the horizontal gridlines.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
plt.plot(range(10))
KITE.stop_prelude()

axes = plt.gca()
axes.yaxis.grid()

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
## Use [`matplotlib.pyplot.grid()`](kite-sym:matplotlib.pyplot.grid) to plot horizontal gridlines along with vertical gridlines in a graph {#use-grid}
Call [`matplotlib.pyplot.grid()`](kite-sym:matplotlib.pyplot.grid) to plot  horizontal and vertical gridlines in the graph.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
plt.plot(range(10))
KITE.stop_prelude()

plt.grid()

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
