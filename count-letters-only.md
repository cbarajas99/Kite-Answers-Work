headers:
  use-count: Use `str.count()`
---
# How to count the number of characters in a string except the spaces in Python
Counting the number of characters in a string except spaces returns the number of letters in the word represented by the string.

## Use [`str.count()`](kite-sym:builtins.str.count) to count the number of character in a string except the spaces {#use-count}
Use [`len(object)`](kite-sym:builtins.len) to get the length of a string `object`. Use [`str.count(sub)`](kite-sym:builtins.str.count) with `sub` as `" "` to count the number of spaces in the same string `str`. Subtract the number of spaces in the string from the length of the string to get the number of letters.

```python
a_string = " hello world "

number_of_letters = len(a_string) - a_string.count(" ")

print(letters)
```
