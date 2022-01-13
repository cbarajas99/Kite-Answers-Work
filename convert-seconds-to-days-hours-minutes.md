headers:
  use-subtraction-floor-division: Use subtraction and floor division
---
# How to convert seconds to days, hours, and minutes in Python
Converting seconds to days, hours, and minutes results in the amount of days, hours, and minutes in a specified number of seconds. For example, 208920 seconds equals 2 days, 10 hours, and 2 minutes.

## Use subtraction and floor division to convert seconds to days, hours, and minutes {#use-subtraction-floor-division}
Use `60 * 60 * 24`, `60 * 60`, and `60` to find the number of  seconds in a day, month, and year, respectively, and store each result in a variable. Use `seconds // seconds_in_day` with `seconds` as the specified number of seconds to determine the number of days. Use `(seconds - (days * seconds_in_day)) // seconds_in_hour` with `days` as the previous result to determine the number of hours. Use `(seconds - (days * seconds_in_day) - (hours * seconds_in_hour)) // seconds_in_minute` with `hours` as the previous result to determine the number of minutes.

```python
seconds = 208920
seconds_in_day = 60 * 60 * 24
seconds_in_hour = 60 * 60
seconds_in_minute = 60

days = seconds // seconds_in_day
hours = (seconds - (days * seconds_in_day)) // seconds_in_hour
minutes = (seconds - (days * seconds_in_day) - (hours * seconds_in_hour)) // seconds_in_minute

print(days, hours, minutes)
```
