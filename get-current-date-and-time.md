headers:
  use-now: Use `datetime.datetime.now()`
  use-time-and-date: Use `datetime.time()` and `datetime.date()`
---
# How to get the current date and current time in Python
Getting the current date and current time can result in a [`datetime.datetime`] object that contains the current date and time or a [`datetime.date`] object that represents the current date and a [`datetime.time`] object that represents the current time.

## Use [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to get the current date and time {#use-now}
Call [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to get a [`datetime.datetime`](kite-sym:datetime.datetime) object that contains the current date and time.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

current_date_and_time = datetime.datetime.now()
print(current_date_and_time)
```

## Use [`datetime.time()`](kite-sym:datetime.time) and [`datetime.date()`](kite-sym:datetime.date) to get the current date and current time separately {#use-time-and-date}
Call [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to get a [`datetime.datetime`](kite-sym:datetime.datetime) object that contains the current date and time. Use [`datetime.date()`](kite-sym:datetime.date) on the [`datetime.datetime`](kite-sym:datetime.datetime) object to get the current date. Use [`datetime.time()`](kite-sym:datetime.time) on the [`datetime.datetime`](kite-sym:datetime.datetime) object to get the current time.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

current_date_and_time = datetime.datetime.now()

current_date = current_date_and_time.date()
print(current_date)

current_time = current_date_and_time.time()
print(current_time)
```
