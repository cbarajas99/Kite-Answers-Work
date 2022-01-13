headers:
  use-sub: Use `re.sub()`
---
# How to remove all non-alphabet characters from a string in Python
Removing all non-alphabet characters from a string results in the string with only alphabet characters. For example, removing all non-alphabet characters from `"a1b2c3!"` results in `"abc"`.

## Use [`re.sub()`](kite-sym:re.sub) to remove all non-alphabet characters from a string {#use-sub}
Call [`re.compile(pattern)`](kite-sym:re.compile) with `pattern` as `"[^a-zA-Z]"` to get a regular expression object. Call [`re.sub(pattern, replacement, string)`](kite-sym:re.sub) with `pattern` as the result of the previous step and `replacement` as `""` to remove all the non-alphabet characters in `string`.

```python
KITE.start_prelude()
import re
KITE.stop_prelude()

a_string = "a1b2c3!"

alphabet_regular_expression = re.compile("[^a-zA-Z]")
string_without_non_alphabet = re.sub(alphabet_regular_expression,"",a_string)

print(string_without_non_alphabet)
```
