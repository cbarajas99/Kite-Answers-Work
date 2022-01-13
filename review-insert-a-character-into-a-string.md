headers:
  use-concatenation: Use concatenation
---
# How to insert a character into a string at an index in Python
Inserting a character at an index of a string creates a new string with the character at the index, and the remainder of the string shifted to the right. For example, inserting `"b"` and index `1` of `"ac"` results in `"abc"`.

## Use concatenation to insert a character into a string at an index {#use-concatenation}
To insert a character into a string at index `i`, split the string using the slicing syntax `a_string[:i]` and `a_string[i:]`. Between these two portions of the original string, use the concatenation operator `+` to insert the desired character. Assign the result to the variable that held the original string.

```python
a_string = "ac"

# insert "b" in the middle of a_string
a_string = a_string[:1] + "b" + a_string[1:]

print(a_string)
```

More than one character can also be inserted.

```python
a_string = "ad"

# insert "bc" in the middle of a_string
a_string = a_string[:1] + "bc" + a_string[1:]

print(a_string)
```
