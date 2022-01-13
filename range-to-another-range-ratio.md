headers:
  use-arithmetic: Use arithmetic operators
---
# How to convert a number within a range to another value in a new range in Python
Converting a value within a range to another value in a new range results in new value that has maintained its ratio. For example, converting `3` in the range `1-5` to another value in the new range `5 - 25` results in `15`.

## Use arithmetic operators to convert a number within a range to another value in a new range {#use-arithmetic}
Subtract the minimum number from the maximum number of the original range to get the old range and repeat with the minimum and maximum in the new range to get the new range. Subtract the minimum in the original range from the old number that will be converted. Multiply this previous results by the new range. Divide the previous result by the old range. Add the new minimum to the previous result.
```python
old_maximum = 5
old_minimum = 1
old_number = 3
new_maximum = 25
new_minimum = 5

old_range = (old_maximum - old_minimum)
new_range = (new_maximum - new_minimum)

new_number = (((old_number - old_minimum) * new_range) / old_range) + new_minimum

print(new_number)
```
