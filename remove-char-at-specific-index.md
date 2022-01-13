headers:
  use-slicing: Use string slicing
---
# How to remove a character from a string at a specific index in Python
Removing a character from a string at a specific index results in a new string that excludes that character. For example, removing the character at index `3` from `"Helllo"` results in `"Hello"`.

## Use string slicing to remove a character from a string at a specific index {#use-slicing}
Use the string slicing and concatenation syntax `a_string[:index] + a_string[index + 1:]` to return a new string equal to `a_string` with the character at `index` removed.
```python
a_string = "Helllo"
index = 3

string_without_character = a_string[:index] + a_string[index + 1:]

print(string_without_character)
```

> **Further reading:**
> Strings support a slicing syntax to access their characters. You can read more about string slicing and string concatenation [here](https://docs.python.org/3/tutorial/introduction.html#strings).
