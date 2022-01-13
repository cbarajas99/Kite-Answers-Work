headers:
  use-strptime: Use `datetime.datetime.strptime()``
---
# How to convert a time string to seconds in Python
Converting a time string to seconds results in the total amount of seconds that represent the time string. For example, converting `"01:01:09"` to seconds results in `3669.0`.

## Use [`datetime.datetime.strptime()`](kite-sym:datetime.datetime.strptime) to convert a time string to seconds {#use-strptime}
Call [`datetime.datetime.strptime(time_string, format)`](kite-sym:datetime.datetime.strptime) where `time_string` is the time in string format and `format` is the format code of the string to return a [`datetime.datetime`](kite-sym:datetime.datetime) object for the time string. Use [`datetime.datetime(year, month, day)`](kite-sym:datetime.datetime) with `year` as `1900`, `month` as `1`, and `day` as `1` to create a [`datetime.datetime`](kite-sym:datetime.datetime) object. Subtract the previous [`datetime.datetime`](kite-sym:datetime.datetime) object from the [`datetime.datetime`](kite-sym:datetime.datetime) object from the time string to get a [`datetime.timedelta`] object . Call [`datetime.timedelta.total_seconds()`](kite-sym:datetime.timedelta.total_seconds) on the [`datetime.timedelta`](kite-sym:datetime.timedelta) object to get the total amount of seconds.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

time_string = "01:01:09"

date_time = datetime.datetime.strptime(time_string, "%H:%M:%S")
print(date_time)
a_timedelta = date_time - datetime.datetime(1900, 1, 1)
seconds = a_timedelta.total_seconds()

print(seconds)
```

> **Further reading:**
> A time string must be of acceptable format to be accepted by [`datetime.strptime()`](kite-sym:datetime.datetime.strptime), read [here](https://www.programiz.com/python-programming/datetime/strptime) to  learn more about format codes.
