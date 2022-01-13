headers:
  use-timedelta: Use `datetime.timedelta()`
---
# How to create a range of dates in Python
Creating a range of dates results in a list of [`datetime.date`](kite-sym:datetime.datetime) objects where each date is sequential to the starting date. For instance, a five day range starting at `2019-09-30` results in `['2019-09-30', '2019-10-01', '2019-10-02', '2019-10-03', '2019-10-04']`.

## Use [`datetime.timedelta()`](kite-sym:datetime.timedelta) to create a range of dates {#use-timedelta}
Use a for-loop to iterate through [`range(stop)`](kite-sym:builtins.range) where `stop` is the wanted number of days. Use the `+` operator to add [`datetime.timedelta(days)`](kite-sym:datetime.timedelta) to the starting [`datetime.date`](kite-sym:datetime.date). `days` is the number of days per for loop created by the range. Use [`date.isoformat()`](kite-sym:datetime.date.isoformat) to convert the created [`datetime.date`](kite-sym:datetime.date) to ISO format. Append the [`datetime.date`](kite-sym:datetime.date) in ISO format to a list.

```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

start_date = datetime.date(2019, 9, 30)
number_of_days = 5

date_list = []
for day in range(number_of_days):
  a_date = (start_date + datetime.timedelta(days = day)).isoformat()
  date_list.append(a_date)

print(date_list)

```
Use list comprehension for a more compact implementation.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

start_date = datetime.date(2019, 9 , 30)
number_of_days = 5

date_list = [(start_date + datetime.timedelta(days = day)).isoformat() for day in range(number_of_days)]

print(date_list)
```
