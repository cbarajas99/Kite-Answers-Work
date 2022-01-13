headers:
  use-choice: Use `random.choice()`
---
# How to create a random string in Python
Creating a random string results in a string containing random lowercase ASCII letters and digits.

## Use [`random.choice()`](kite-sym:random.choice) to create a random string {#use-choice}
Concatenate the results of [`string.ascii_lowercase`](kite-sym:string.ascii_lowercase) and [`string.digits`](kite-sym:string.digits) to obtain all ASCII characters and digits. Use a for-loop and [`range(stop)`](kite-sym:builtins.range) to begin creating a string of length `stop-1`. In each iteration, use [`random.choice(seq)`](kite-sym:random.choice) with the `seq` as the ASCII characters and digits to obtain a random item.

```python
KITE.start_prelude()
import random
import string
random.seed(0)
KITE.stop_prelude()

length_of_string = 5

letters_and_digits = string.ascii_lowercase + string.digits
random_string = ""
for number in range(length_of_string):
  random_string += random.choice(letters_and_digits)

print(random_string)
```
