headers:
  use-imshow: Use `matplotlib.pyplot.imshow()`
---
# How to display an image as grayscale using Matplotlib in Python
Displaying an image as grayscale using [`Matplotlib`](kite-sym:matplotlib) results in graph containing the image in grayscale.

## Use [`matplotlib.pyplot.imshow()`](kite-sym:matplotlib.pyplot.imshow) to display an image as grayscale using Matplotlib in Python
Use [`PIL.Image.open(fp)`](kite-sym:PIL.Image.open) to open and identify the image file `fp`. Call [`PIL.Image.Image.convert(mode)`] with `PIL.Image.Image` as the opened image file and `mode` as `"L"` to convert it to a grayscale image. Use [`numpy.asarray(a)`](kite-sym:numpy.core.numeric.asarray) with `a` as the grayscale image to convert it to an array. Call [`matplotlib.pyplot.imshow(X, cmap)`] with `X` as the previous array and `cmap` as `cmap="gray"`.
```python
KITE.start_prelude()
import PIL.Image
import numpy as np
import matplotlib.pyplot as plt
KITE.write_sample_file("sample1.png", dst="sample.png")
KITE.display_image("sample.png")
KITE.stop_prelude()

open_image = PIL.Image.open("sample.png")
grayscale = open_image.convert("L")

arr = np.asarray(grayscale)
plt.imshow(arr, cmap='gray')

KITE.set_display_code(False)
plt.savefig("sample.png")
KITE.display_image("sample.png")
KITE.set_display_code(True)
```
