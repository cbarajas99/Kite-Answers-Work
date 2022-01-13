headers:
  use-timedelta: Use `datetime.timedelta()`
---
# How to add time onto a datetime.datetime object in Python
Adding time to a [`datetime.datetime`](kite-sym:datetime.datetime) object results in a new [`datetime.datetime`](kite-sym:datetime.datetime) object with updated time information. For example, adding `10 hours` to a [`datetime.datetime`](kite-sym:datetime.datetime) object containing `2020-02-19 12:00:00` creates a new [`datetime.datetime`](kite-sym:datetime.datetime) object with `2020-02-19 22:00:00`.

## Use [`datetime.timedelta()`](kite-sym:datetime.timedelta) to add time to a [`datetime.datetime`](kite-sym:datetime.datetime) object {#use-timedelta}
Call [`datetime.timedelta(duration=n)`](kite-sym:datetime.timedelta) with `duration` as weeks, days, hours, minutes, seconds, microseconds, or milliseconds and `n` as a specified amount of time to create a [`datetime.timedelta`](kite-sym:datetime.timedelta) object representing the specified duration. Add this object to a [`datetime.datetime`](kite-sym:datetime.datetime) object to add create a new [`datetime.datetime`](kite-sym:datetime.datetime) object with the added time.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date_and_time = datetime.datetime(2020, 2, 19, 12, 0, 0)
print(date_and_time)

time_change = datetime.timedelta(hours=10)
new_time = date_and_time + time_change

print(new_time)
```
