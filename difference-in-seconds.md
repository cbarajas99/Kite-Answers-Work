headers:
  use-total-seconds: Use `datetime.timedelta.total_seconds()`
---
# How to get the difference in seconds between two datetime.date objects in Python
Getting the difference in seconds between two [`datetime.date`](kite-sym:datetime.date) objects results in a [`datetime.timedelta`](kite-sym:datetime.timedelta) object that represents the difference between them. For example, the difference between `2015-07-14` and `2015-05-18` results in `4924800.0`.

## Use [`datetime.timedelta.total_seconds()`](kite-sym:datetime.timedelta.total_seconds) to get the difference in seconds between two [`datetime.date`](kite-sym:datetime.date) objects {#use-total-seconds}
Subtract one [`datetime.date`](kite-sym:datetime.date) from another to return a [`datetime.timedelta`](kite-sym:datetime.timedelta) containing the time difference between two dates. Call [`datetime.timedelta.seconds()`](kite-sym:datetime.timedelta.seconds) to return the difference in seconds.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date1 = datetime.date(2015, 7, 14)
date2 = datetime.date(2015, 5, 18)

a_timedelta = date1 - date2
seconds = a_timedelta.total_seconds()

print(seconds)
```
