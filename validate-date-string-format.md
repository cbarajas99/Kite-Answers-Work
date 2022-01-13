heheaders:
  use-try-except: Use a try and except block
---
# How to validate a date string format in Python
Validating that a date string is of a certain format results in getting told if the date string is of the correct format, and if not, it tells which date format it should be. For example, validating to see if `'12-25-2018'` is of the format `YYYY-MM-DD` results in `"This is the incorrect string data format. It should be YYYY-MM-DD"`.

## Use a try and except block to validate a date string format {#use-try-except}
Use a try and except block. In the try block, call [`datetime.datetime.strptime(date_string, format)`](kite-sym:datetime.datetime.strptime) with `date_string` as the date string to see if it is in the acceptable desired `format` and print a message saying the date string is in the correct format. If it's not the correct format, then it will raise a `Value Error`. In the except block, catch the `ValueError` then print a message saying the date string is in the incorrect format and what format it should be instead.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date_string = '12-25-2018'
format = "%Y-%m-d"

try:
  datetime.datetime.strptime(date_string, format)
  print("This is the correct date string format.")
except ValueError:
  print("This is the incorrect date string format. It should be YYYY-MM-DD")
```
> **Further reading:**
> A date string must be of acceptable format to be accepted by [`datetime.strptime()`](kite-sym:datetime.datetime.strptime). [Read more about the different format codes here.](https://www.programiz.com/python-programming/datetime/strptime)
