headers:
  use-string-concatenation: Use string concatenation
---
# How to insert characters at the start and end of a string in Python
Inserting characters at the start and end of a string results in a new string with characters prepended and appended to the string.

## Use string concatenation to insert characters at the start and end of a string {#use-string-concatenation}
Use the `+` operator to concatenate characters before and after a string.
```python
string1 = "c"

string2 = "ab" + string1 + "de"

print(string2)
```
