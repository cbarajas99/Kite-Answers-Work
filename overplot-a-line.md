headers:
  use-polyfit: Use `numpy.polyfit()`
---
# How to plot a linear regression line on a scatter plot in Python
Plotting a linear regression line on a scatter plot displays a scatter plot of data along with a line of best fit for the data.

## Use [`numpy.polyfit()`](kite-sym:numpy.polyfit) to plot a linear regression line on a scatter plot {#use-polyfit}
Call [`numpy.polyfit(x, y, degree)`](kite-sym:numpy.polyfit) with `x` and `y` as arrays of x and y-values of the scatter plot, and `degree` as `1` to calculate the slope and y-intercept of the line of the best fit. Plot the a linear regression line by calling[`matplotlib.pyplot.plot(x, eq)`](kite-sym:matplotlib.pyplot.plot) with `x` as the array of x-values for the scatter plot and `eq` as the y-intercept added to the product of the slope and x.
```python
KITE.start_prelude()
import matplotlib.pyplot as plt
import numpy as np
KITE.stop_prelude()
# generate data
x = np.array([1, 3, 5, 7])
y = np.array([ 6, 3, 9, 5 ])
#create scatter plot
plt.plot(x, y, 'o')

#m = slope, b = intercept
m, b = np.polyfit(x, y, 1)
#add line of best fit
plt.plot(x, m*x + b)

KITE.set_display_code(False)
plt.savefig("sample_plot.jpg")
KITE.display_image("sample_plot.jpg")
KITE.set_display_code(True)
```
