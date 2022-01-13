headers:
  use-strptime: Use `datetime.datetime.strptime()`
---
# How to convert a date string to a date object in Python
Converting a date string to a date object converts a date string of acceptable format to a [`datetime.date`](kite-sym:datetime.date) object. For instance, converting `28022019` results in `2019-02-28`.

## Use [`datetime.datetime.strptime()`](kite-sym:datetime.datetime.strptime) to convert a date string to a date object {#use-strptime}
Use [`datetime.datetime.strptime(string, format)`](kite-sym:datetime.datetime.strptime) with a date string as `string` with an acceptable `format` to get a [`datetime.datetime`](kite-sym:datetime.datetime) object. Use [`datetime.date()`](kite-sym:datetime.date) to convert the [`datetime.datetime`](kite-sym:datetime.datetime) object to a [`datetime.date`](kite-sym:datetime.date) object.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

# %d%m%Y follows the structure of the string
str_to_datetime = datetime.datetime.strptime("28022019","%d%m%Y")
datetime_to_date = str_to_datetime.date()

print(datetime_to_date)
```
> **Further reading:**
> A date string must be of acceptable format to be accepted by [`datetime.strptime()`](kite-sym:datetime.datetime.strptime). [Read more about the different format codes here.](https://www.programiz.com/python-programming/datetime/strptime)
