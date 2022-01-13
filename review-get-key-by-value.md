headers:
  use-for-loop: Use a for loop
---
# How to get a key from a value in a dictionary
In a dictionary, each key is paired with a value. For example, the key `"b"` is paired with the value `2` in `{"a": 1, "b": 2}`. Key-value pairs can only be accessed through the key. But, it is possible to iterate through the key-value pairs of a dictionary.

## Use a for loop to get a key from a value {#use-for-loop}
Call [`dict.items()`](kite-sym:builtins.dict.items) with a dictionary as `dict` to iterate through all dictionary entries in a loop. Use two variables in the loop, one representing a key and the other a value. Use a conditional statement that checks if the desired value equals the value of the current iteration.

```python
a_dictionary = {"a": 1, "b": 2}
search_value = 2

for key, value in a_dictionary.items():
    if search_value == value:
        # gets key of value
        found_key = key
        break

print(found_key)
```

For a more compact implementation, use a list comprehension. This approach results in a list of matching keys.

```python
a_dictionary = {"a": 1, "b": 2}
search_value = 2

# lists of all keys with specific value
found_key = [key for key, value in a_dictionary.items() if value == search_value]

print(found_key)
```
