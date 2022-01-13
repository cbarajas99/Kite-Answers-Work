headers:
  use-combine: Use `datetime.datetime.combine()`
---
# How to subtract two datetime.time objects in Python
Subtracting two [`datetime.time`](kite-sym:datetime.time) objects results in a [`datetime.timedelta`](kite-sym:datetime.timedelta) object that represents the difference between them. For example, subtracting `13:35:50` from `15:30:35` results in `2:54:45`.

## Use [`datetime.datetime.combine()`](kite-sym:datetime.datetime.combine) to subtract two [`datetime.time`](kite-sym:datetime.time) objects {#use-combine}
Use [`datetime.date(year, month, day)`](kite-sym:datetime.date) with any valid entries as `year`, `month`, and `day` to create a [`datetime.date`](kite-sym:datetime.date) object. Call [`datetime.datetime.combine(date, time)`](kite-sym:datetime.datetime.combine) to combine the previous result `date` with the first [`datetime.time`](kite-sym:datetime.time) `time`. Repeat this step using the second [`datetime.time`](kite-sym:datetime.time). Use `time2 - time1` to find the difference between the previous two results `time2` and `time1`.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

start_time = datetime.time(15, 30, 35)
stop_time = datetime.time(13, 35, 50)

date = datetime.date(1, 1, 1)
datetime1 = datetime.datetime.combine(date, start_time)
datetime2 = datetime.datetime.combine(date, stop_time)
time_elapsed = datetime1 - datetime2

print(time_elapsed)
```
