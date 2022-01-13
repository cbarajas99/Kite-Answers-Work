headers:
  use-datetime-now: Use `datetime.datetime.now()`
---
# How to create a file name with the current date and time in python
Creating a file name with current date and time results in an empty file whose name is the current date and time.

## Use [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to create a file name with the current date and time {#use-datetime-now}
Use [`datetime.datetime.now()`](kite-sym:datetime.datetime.now) to get a [`datetime.datetime`](kite-sym:datetime.datetime) with the current date and time. Use [`str()`](kite-sym:builtins.str) to convert the [`datetime.datetime`](kite-sym:datetime.datetime) to a string. Use `+` to concatenate the string with `".txt"`. Use [`open(file, mode)`](kite-sym:builtins.open) with the file name string as `file` and `mode` as `"w"` to open the file for writing. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.
```python
KITE.start_prelude()
import datetime
KITE.stop_prelude()

current_date_and_time = datetime.datetime.now()
current_date_and_time_string = str(current_date_and_time)

file_name =  current_date_and_time + ".txt"
file = open(file_name, 'w')
file.close()

KITE.set_display_code(False)
KITE.write_file(file_name, " ")
KITE.display_file(file_name)
KITE.set_display_code(True)
```
