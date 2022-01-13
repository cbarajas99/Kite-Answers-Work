headers:
  use-sys-write: Use `sys.stdout.write()`
---
# How to show a progress bar in Python
Showing a progress bar prints status bars on separate lines with percentages representing progress to `100%`.

## Use [`sys.stdout.write()`](kite-sym:builtins.file.write) to show a progress bar {#use-sys-write}
Call [`range(stop)`](kite-sym:builtins.range) with `stop` as the desired number of progress bars plus `1`. Use a for-loop to iterate through this range. At each iteration, call [`sys.stdout.write(data)`](kite-sym:builtins.file.write) with `data` as string formatting as `"[%-nums]  %d%%" % ('=' * i, progress  * i)` with `num` as the desired number of progress bars, `progress` as the result of 100 divided by `num`, and `i` as the variable of the range that is being iterated through. Call [`sys.stdout.write(data)`](kite-sym:builtins.file.write) with `data` as `"\n"` to make the next progress bar show on the next line. Call [`time.sleep(seconds)`](kite-sym:time.sleep) with `seconds` as the desired number of seconds before it shows the next progress bar.
```python
KITE.start_prelude()
import time
import sys
KITE.stop_prelude()

for i in range(11):
    sys.stdout.write("[%-10s] %d%%" % ('='*i, 10*i))
    sys.stdout.write('\n')
    time.sleep(0.25)
```
