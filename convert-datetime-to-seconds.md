headers:
  use-total-seconds: Use `datetime.timedelta.total_seconds()`
---
# How to convert the difference between two datetime objects to seconds in Python
Converting the difference between two [`datetime.datetime`](kite-sym:datetime.datetime) objects returns the total amount of seconds between the two.

## Use `datetime.timedelta.total_seconds()` to convert the difference between two `datetime` objects to {#use-total-seconds}
Subtract the most recent [`datetime.datetime`](kite-sym:datetime.datetime) from the older [`datetime.datetime`](kite-sym:datetime.datetime) to create a [`datetime.timedelta`](kite-sym:datetime.timedelta) that contains the time difference between the two. Use [`timedelta.total_seconds()`](kite-sym:datetime.timedelta.total_seconds) to get the total amount of seconds.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date_and_time1 = datetime.datetime(2009, 10, 21, 0, 0, 0)
date_and_time2 = datetime.datetime(2008, 10, 21, 0, 0, 0)

a_timedelta = date_and_time1 - date_and_time2
seconds = a_timedelta.total_seconds()

print(seconds)
```
