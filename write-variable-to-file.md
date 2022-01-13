headers:
  use-string-concatenation: Use string concatenation
  use-string-formatting: Use string formatting
---
# How to write a variable to a file in Python
Writing a variable to a file results in a file containing the variable name and the value.

## Use string concatenation to write a variable to file {#use-string-concatenation}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"w"` to open the file for writing. Use [`repr(object)`](kite-sym:builtins.repr) with `object` as the variable to convert the variable to a string.
Call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as a string concatenation of three things: a string containing the variable name and `=`, the string version of the variable, and `"\n"`. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
a_dictionary = {'a' : 1, "b" : 2}

file = open("sample.txt", "w")
str_dictionary = repr(a_dictionary)
# "\n" creates newline for next write to file
file.write('a_dictionary = ' + str_dictionary + "\n")
file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
## Use string formatting to write a variable to file {#use-string-formatting}
Use [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"w"` to open the file for writing. Call [`file.write(data)`](kite-sym:builtins.file.write) with `data` as the string formats `"%s %d"` followed by `%` and a tuple containing a string of the variable name, and the variable. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
a_dictionary = {'a' : 1, "b" : 2}

file = open("sample.txt", "w")
file.write('%s = %s\n' %("a_dictionary", a_dictionary))
file.close()

KITE.set_display_code(False)
KITE.display_file("sample.txt")
KITE.set_display_code(True)
```
