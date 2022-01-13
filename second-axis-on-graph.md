headers:
  use-twiny: Use `matplotlib.axes._base._AxesBase.twiny()`
---
# How to add a second x-axis in a Matplotlib graph in Python
Adding a second x-axis results in a [`Matplotlib`](kite-sym:matplotlib) graph that contains the top and bottom x-axis labeled sharing one labeled y-axis.

## Use [`matplotlib.axes._base._AxesBase.twiny()`](kite-sym:matplotlib.axes._base._AxesBase.twiny) to add a second x-axis in a Matplotlib graph {#use-twiny}
Use [`matplotlib.pyplot.gca()`](kite-sym:matplotlib.pyplot.gca) to get the current axes of the graph. Call [`matplotlib.axes._base._AxesBase.twiny()`](kite-sym:matplotlib.axes._base._AxesBase.twiny) on the current axes to create a twin of axes that have a shared y-axis with the current axes. Call [`matplotlib.axes._axes.Axes.set_xticks(ticks)`](kite-sym:matplotlib.axes._axes.Axes.set_xticks) with `ticks` as a list of floats to set the x-ticks on the twin axes. Call [`matplotlib.axes._axes.Axes.set_xlabel(xlabel)`](kite-sym:matplotlib.axes._axes.Axes.set_xlabel) with `xlabel` as the label for the x-axis for the original axes and twin axes.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
plt.plot(range(10))
KITE.stop_prelude()

axes1 = plt.gca()
axes2 = axes1.twiny()

axes2.set_xticks([.33, .66, .99])

axes1.set_xlabel("x-axis 1")
axes2.set_xlabel("x-axis 2")


KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
