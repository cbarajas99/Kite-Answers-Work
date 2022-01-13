headers:
  use-timedelta-days-and-timedelta-seconds: Use `timedelta.days` and `timedelta.seconds`
---
# How to convert a timedelta to days, hours, and minutes in Python
A [`datetime.timedelta`](kite-sym:datetime.timedelta) object contains `days`, `seconds`, and `microseconds`, but when called returns the `days` and `time` of the object. Getting the `days` from a [`timedelta`](kite-sym:datetime.timedelta) is direct in Python. Getting the hours and minutes from a [`timedelta`](kite-sym:datetime.timedelta) requires division. For example, converting `timedelta(days = 20, seconds = 31949, microseconds = 0)` to days, hours, and minutes returns `days: 20 hours: 8 minutes: 52`.

## Use [`timedelta.days`](kite-sym:datetime.timedelta.days) and [`timedelta.seconds`](kite-sym:datetime.timedelta.seconds)  to convert a [`timedelta`](kite-sym:datetime.timedelta) to days, hours, and minutes {#use-timedelta-days-and-timedelta-seconds}
Call [`timedelta.days`](kite-sym:datetime.timedelta.days)  to get the days. Call and divide [`timedelta.seconds`](kite-sym:datetime.timedelta.seconds) to get the hours and minutes.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

days_and_time = datetime.timedelta(days = 20, seconds = 31949, microseconds = 0)
print(days_and_time)

days = days_and_time.days
hours = days_and_time.seconds//3600
minutes = (days_and_time.seconds//60)%60
print("days:", days_and_time.days, "hours:", days_and_time.seconds//3600, "minutes:", (days_and_time.seconds//60)%60)
```
