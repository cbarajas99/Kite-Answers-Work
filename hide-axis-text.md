headers:
  use-setvisible: Use `matplotlib.axes.axes.set_visible()`
  use-setticklabels: Use `matplotlib.axes.xaxis.set_ticklabels()` and `matplotlib.axes.yaxis.set_ticklabels()`
---
# How to hide axis text in Matplotlib graphs in Python
Hiding axis text results in a [`Matplotlib`](kite-sym:matplotlib) graph where the axes have no labels.

## Use [`matplotlib.axes.Axes.set_visible()`](kite-sym:matplotlib.axes.Axes.set_visible) to hide axis text and ticks {#use-setvisible}
Call [`matplotlib.pyplot.gca()`](kite-sym:matplotlib.pyplot.gca) to get the current axes of the graph. Use [`matplotlib.axes.Axes.get_xaxis()`](kite-sym:matplotlib.axes._axes.Axes.get_xaxis) or [`matplotlib.axes.axes.get_yaxis()`](kite-sym:matplotlib.axes._axes.Axes.get_yaxis) to get the x or y-axes, respectively. On both axes, call [`matplotlib.axes.Axes.set_visible(boolean)`](kite-sym:matplotlib.axes.Axes.set_visible) with `boolean` as `False` to remove all text and ticks from the figure.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
KITE.stop_prelude()

plt.plot(range(5))

figure = plt.gca()

x_axis = figure.axes.get_xaxis()
x_axis.set_visible(False)

y_axis = figure.axes.get_yaxis()
y_axis.set_visible(False)

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
## Use [`matplotlib.axes.xaxis.set_ticklabel()`](kite-sym:matplotlib.axis.XAxis.set_ticklabels) and [`matplotlib.axes.yaxis.set_ticklabel()`](kite-sym:matplotlib.axis.YAxis.set_ticklabels) to hide axis text {#use-setticklabels}
Call [`matplotlib.pyplot.gca()`](kite-sym:matplotlib.pyplot.gca) to get the current axes of the graph. Use [`matplotlib.axes.xaxis.set_ticklabel(object)`](kite-sym:matplotlib.axis.XAxis.set_ticklabels) or [`matplotlib.axes.yaxis.set_ticklabel(object)`](kite-sym:matplotlib.axis.YAxis.set_ticklabels) with `object` set to `[]` to hide axis text.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
KITE.stop_prelude()

plt.plot(range(5))

figure = plt.gca()

figure.axes.xaxis.set_ticklabels([])
figure.axes.yaxis.set_ticklabels([])

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
