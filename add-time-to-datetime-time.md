headers:
  use-combine: Use `datetime.datetime.combine()`
---
# How to add a datetime.timedelta object to a datetime.time in Python
Adding a [`datetime.timedelta`](kite-sym:datetime.timedelta) object to a [`datetime.time`](kite-sym:datetime.time) results in a new [`datetime.time`](kite-sym:datetime.time) object. For example, adding `1:05:25` to `13:40:10` results in `14:45:35`.

## Use [`datetime.datetime.combine()`](kite-sym:datetime.datetime.combine) to add a [`datetime.timedelta`](kite-sym:datetime.timedelta) object to a [`datetime.time`](kite-sym:datetime.time) object {#use-combine}
Call [`datetime.datetime.combine(date, time)`](kite-sym:datetime.datetime.combine) with `date` as any [`datetime.date`](kite-sym:datetime.date) object and `time` as the [`datetime.time`](kite-sym:datetime.time) object to create a [`datetime.datetime`](kite-sym:datetime.datetime) object. Add the previous [`datetime.datetime`](kite-sym:datetime.datetime) object with the [`datetime.timedelta`](kite-sym:datetime.timedelta) object to add more time. Call [`datetime.time()`](kite-sym:datetime.time) on the previous result to get the new [`datetime.time`](kite-sym:datetime.time) object.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

time = datetime.time(13,40,10)
added_time = datetime.timedelta(hours = 1, minutes = 5, seconds = 25)

date_and_time = datetime.datetime.combine(datetime.date.today(), time)
new_date_and_time = date_and_time + added_time
new_time = new_date_and_time.time()

print(new_time)
```
