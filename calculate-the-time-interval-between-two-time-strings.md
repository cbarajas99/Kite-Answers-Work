headers:
  use-strptime: Use `datetime.strptime()`
---
# How to calculate the time interval between two time strings in Python
Calculating the time interval between two time strings returns a [`datetime.timedelta`](kite-sym:datetime.timedelta) object that shows the difference between the two times.

## Use [`datetime.strptime()`](kite-sym:datetime.datetime.strptime) to calculate the time interval between two times strings {#use-strptime}
Use [`datetime.datetime.strptime(date_string, format)`](kite-sym:datetime.datetime.strptime) where `date_string` is the time in string format and `format` is the format code of the string to return a [`datetime.datetime`](kite-sym:datetime.datetime) object for each time string. Subtract the later [`datetime.datetime`](kite-sym:datetime.datetime) object from the earlier [`datetime.datetime`](kite-sym:datetime.datetime) object to return their difference as a [`datetime.timedelta`](kite-sym:datetime.timedelta).

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

datetime1 = datetime.datetime.strptime('12:00:00',"%H:%M:%S")
datetime2 = datetime.datetime.strptime('5:17:51',"%H:%M:%S")

time_difference = datetime2 - datetime1

print(time_difference)
```
