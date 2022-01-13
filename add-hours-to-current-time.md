headers:
  use-timedelta: Use `datetime.timedelta()`
---
# How to add hours to the current time in Python
Adding hours to the current time results in a new [`datetime.datetime`](kite-sym:datetime.datetime) object with the added hours.

## Use [`datetime.timedelta()`](kite-sym:datetime.timedelta) to add hours to the current time {#use-timedelta}
Call [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to get the current date and time. Use [`datetime.timedelta(hours)`](kite-sym:datetime.timedelta) with `hours` set equal to the desired added hours to convert `hours` to a [`datetime.timedelta`](kite-sym:datetime.timedelta) object. Add the current [`datetime.datetime`](kite-sym:datetime.datetime) object with the previous [`datetime.timedelta`](kite-sym:datetime.timedelta) object to create a new [`datetime.datetime`](kite-sym:datetime.datetime) object with the added hours.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

current_date_and_time = datetime.datetime.now()
print(current_date_and_time)

hours = 5
hours_added = datetime.timedelta(hours = hours)

future_date_and_time = current_date_and_time + hours_added

print(future_date_and_time)
```
