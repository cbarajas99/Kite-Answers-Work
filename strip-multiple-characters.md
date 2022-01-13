headers:
  use-replace: Use `str.replace()`
  use-sub: Use `re.sub()`
---
# How to remove multiple characters from a string in Python
Removing multiple characters from a string results in a new string that excludes those characters. For example, removing `"!()@"` from `"!(Hell@o)"` results in `"Hello"`.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to remove multiple characters from a string {#use-replace}
Create a copy of the original string. Put the multiple characters that will be removed in one string. Use a for-loop to iterate through each character of the previous result. At each iteration, call [`str.replace(old, new)`] with `old` as the character and `new` as `""` to replace `old` with `new` in the copy of the original string. Then, assign the copy of the original string to be the previous result.
```python
original_string = "!(Hell@o)"
characters_to_remove = "!()@"

new_string = original_string
for character in characters_to_remove:
  new_string = new_string.replace(character, "")

print(new_string)
```

## Use [`re.sub()`](kite-sym:re.sub) to remove multiple characters from a strings {#use-sub}
Put the multiple characters that will be removed in one string. Use string concatenation to add `"["` to the front of the string of multiple characters and `"["` to the back of the string. Call [`re.sub(pattern, replace, string)`](kite-sym:re.sub) with `pattern` as the previous result, replace as `""` and `string` as the string whose characters will be removed.
```python
KITE.start_prelude()
import re
KITE.stop_prelude()

original_string = "!(Hell@o)"
characters_to_remove = "!()@"

pattern = "[" + characters_to_remove + "]"
new_string = re.sub(pattern, "", original_string)

print(new_string)
```
