headers:
  use-str-splitlines: Use `str.splitlines()`
  use-str-rstrip: Use `str.rstrip()`
---
# How to split a file into a list in Python
Splitting the file into a list results in a list where each element is a line of the file. For example, splitting a file that contains `"First Line\nSecond Line"` results in `["First Line", "Second Line"]`.

## Use [`str.splitlines()`](kite-sym:builtins.str.splitlines) to split a file into a list {#use-str-splitlines}
Use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Call [`file.read()`](kite-sym:builtins.file.read) to return the entire content of `file` as a string. Call [`str.splitlines()`](kite-sym:builtins.str.splitlines) with `str` as the file content to return a list of the lines in the string, breaking at line boundaries not including line breaks. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
KITE.set_display_code(False)
file = open("sample.txt", "w")
file.write("First Line\nSecond Line")
file.close()
KITE.display_file("sample.txt")
KITE.set_display_code(True)

f = open("sample.txt", "r")
# Get contents of file `f`
content = f.read()
content_list = content.splitlines()
f.close()
print(content_list)
```

## Use [`str.rstrip()`](kite-sym:builtins.str.rstrip) to remove trailing newlines {#use-str-rstrip}
Use [`open(file, mode)`](kite-sym:builtins.open) with `mode` as `"r"` to open `file` for reading. Use a list comprehension to traverse the file's content line by line with a for-loop, and call [`str.rstrip(chars)`](kite-sym:builtins.str.rstrip) with each line as `str` and `chars` as `'\n'`. Use [`file.close()`](kite-sym:builtins.file.close) to close `file`.

```python
KITE.set_display_code(False)
file = open("sample.txt", "w")
file.write("First Line\nSecond Line")
file.close()
KITE.display_file("sample.txt")
KITE.set_display_code(True)

f = open("sample.txt", "r")
content_list = [line.rstrip('\n') for line in f]
f.close()
print(content_list)
```

> **Warning:**
> Removing trailing newlines with [`str.rstrip()`](kite-sym:builtins.str.rstrip) may remove additional characters than the intended.

> **Further reading:**
> List comprehensions provide a concise way to create lists. You can read more about list comprehensions [here](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions).
