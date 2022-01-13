headers:
  use-today: Use `datetime.date.today`
---
# How to check if a datetime.date is the same date as today in Python
Checking if a [`datetime.date`](kite-sym:datetime.date) is the same date as today results in `True` if they are the same date and `False` otherwise.

## Use [`datetime.datetime.today()`](kite-sym:datetime.datetime.today) to check if a [`datetime.date`](kite-sym:datetime.date) object is the same date as today {#use-today}
Call [`datetime.date.today()`](kite-sym:datetime.date.today) to get the `datetime.date` object of today. Use the `==` operator to check if the `datetime.date` object is the same as the `datetime.date` object of today.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

date = datetime.date(2016,6,6)

date_of_today = datetime.date.today()
if date == date_of_today:
    print(True)
else:
    print(False)
```
