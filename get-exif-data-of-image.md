headers:
  use-getexif: Use `PIL.Image.Image.getexif()`
---
# How to get the EXIF data for an image in Python?
EXIF data is stored data in an image file that includes the date the photo was taken, resolution, shutter speed, focal length, and other camera settings. Getting the EXIF data for an image results in a dictionary contain all of the data.

## Use [`PIL.Image.Image.getexif()`](kite-sym:PIL.Image.Image.getexif) to get the EXIF data for an image {#use-getexif}
Use [`PIL.Image.Image.open()`](kite-sym:PIL.Image.open(fp) with `fp` as the filename of the image to return a `PIL.Image.Image` object. Call [`PIL.Image.Image.getexif()`](kite-sym:PIL.Image.Image.getexif) with `PIL.Image.Image` as the previous result to get the EXIF data.
```python
KITE.start_prelude()
import PIL.Image
KITE.write_sample_file("sample4.jpg", dst="sample.jpg")
KITE.display_image("sample.jpg")
KITE.stop_prelude()

image = PIL.Image.open('sample.jpg')

EXIF_data = image._getexif()

print(EXIF_data)
```
