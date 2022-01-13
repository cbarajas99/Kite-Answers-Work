headers:
  use-replace: Use `datetime.datetime.replace()`
  use-isoformat: Use `datetime.datetime.isoformat()`
---
# How to get change a datetime to a datetime without microseconds in Python
Changing a [`datetime.datetime`](kite-sym:datetime.datetime) object to a [`datetime.datetime`](kite-sym:datetime.datetime) object without microseconds results in a [`datetime.datetime`](kite-sym:datetime.datetime) object whose time is hours, minutes, and seconds.

## Use [`datetime.datetime.replace()`](kite-sym:datetime.datetime.replace) to change a datetime to a datetime without microseconds {#use-replace}
Call [`datetime.datetime.replace(microseconds = None)`](kite-sym:datetime.datetime.replace) and set `microseconds` to `0`.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

a_datetime = datetime.datetime(2018, 11, 2, 12, 25, 50, 3030)

datetime_without_microseconds = a_datetime.replace(microsecond = 0)

print(datetime_without_microseconds)
```

## Use [`datetime.datetime.isoformat()`](kite-sym:datetime.datetime.isoformat) to change a datetime to a datetime without microseconds {#use-isoformat}
 Use [`datetime.datetime.isoformat(sep, timespec)`](kite-sym:datetime.datetime.isoformat). `sep` as `" "` and `timespec` as `"seconds"` to remove microseconds.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

a_datetime = datetime.datetime(2018, 11, 2, 12, 25, 50, 3030)

datetime_without_microseconds = a_datetime.isoformat(" ", "seconds")

print(datetime_without_microseconds)
```
