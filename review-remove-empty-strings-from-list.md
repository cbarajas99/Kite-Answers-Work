headers:
  use-filter: Use `filter()`
  use-for-loop: Use a for loop
---
# How to remove empty strings from a list of strings in Python
The empty string `""` contains no characters. Removing empty strings from a list results in a list excluding the empty strings. For example, removing empty strings from `["a", "", "c"]` results in `["a", "c"]`.

## Use a for loop to remove empty strings from a list {#use-for-loop}
Use a for-loop to iterate through the list. At each iteration, check if each string is not an empty string. If it is not an empty string, use [`list.append(object)`](kite-sym:builtins.list.append) to add each non-empty string to an initially empty list.

```python
a_list = ["a", "", "c"]

without_empty_strings = []
for string in a_list:
    if (string != ""):
        # list containing non-empty strings
        without_empty_strings.append(string)

print(without_empty_strings)
```
Use a list comprehension for a more compact solution.
```python
a_list = ["a", "", "c"]

without_empty_strings = [string for string in a_list if string != ""]

print(without_empty_strings)
```
## Use [`filter()`](kite-sym:builtins.filter) to remove empty strings from a list {#use-filter}
Call [`filter(function, iterable)`](kite-sym:builtins.filter) with a lambda function that checks for the empty string as `function` and a list as `iterable`. Use [`list()`](kite-sym:builtins.list) to convert the resultant filter object to a list.

```python
a_list = ["a", "", "c"]

# filter out empty strings
filter_object = filter(lambda x: x != "", a_list)
without_empty_strings = list(filter_object)

print(without_empty_strings)
```
