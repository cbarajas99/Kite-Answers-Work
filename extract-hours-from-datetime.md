headers:
  use-hour: Use `datetime.datetime.hour`
---
# How to get the hours from a datetime.datetime object in Python
Getting the hours from a [`datetime.datetime`](kite-sym:datetime.datetime) object results in an integer that represents the hours in that [`datetime.datetime`](kite-sym:datetime.datetime).

## Use [`datetime.datetime.hour`](kite-sym:datetime.datetime.hour) to get the hours from a [`datetime.datetime`](kite-sym:datetime.datetime) object {#use-hour}
Call [`datetime.datetime.hour`](kite-sym:datetime.datetime.hour) on the [`datetime.datetime`](kite-sym:datetime.datetime) object to get the hours.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date_and_time = datetime.datetime(2020, 1, 6, 13, 25, 50)

hours = date_and_time.hour

print(hours)
```
