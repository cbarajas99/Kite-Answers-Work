headers:
  use-str-format: Use `str.format()`
  use-f-strings: Use f-strings
  use-string-formatting: Use `%`-formatting
---
# How to format strings in Python
Formatting strings allows a specified value to be formatted within a string. For example, the integer `1` formatted to two decimal places within a string results in `"1.00"`.

## Use [`str.format()`](kite-sym:builtins.str.format) to format a string {#use-str-format}
Use [`str.format(*args, *kwargs)`](kite-sym:builtins.str.format) to format `str` using substitutions from `*args` and `*kwargs`. Each substitution is defined by `{field_name:conversion}`, where `field_name` is the index of the substitution in `*args` and `*kwargs` and conversion is the conversion code of the substitution type.

```python
text = 'The number {0:.2f} added with {1:.2f} gives {2:.2f}.'
output = text.format(1, 2, 3)
print(output)
```
## Use f-strings to format a string {#use-f-strings}
Prefix the start of the string to format with `f`, and specify one or more braces `{}` within the string. Each `{}` contains an expression, and are replaced with their values.

```python
name = 'John'
age = 20
text = f'My name is {name} and my current age is {age+1}.'
print(text)
```

## Use `%`-formatting to format strings {#use-string-formatting}
Use the syntax `format % values` to format `values` within the string `format`, where `format` contains one or more `% ` conversion specifications. Each conversion specification will be replaced with the arguments in `values`. If multiple arguments are provided, pass the arguments as a tuple to `values`.

```python
text = "2 raised to the third power is %s." % 8
print(text)
```

> **Further reading:**
> [`str.format()`](kite-sym:builtins.str.format) can be used to format strings. Read more about the conversion codes for [`str.format()`](kite-sym:builtins.str.format) [here](https://docs.python.org/3/library/string.html#format-specification-mini-language).
> F-strings are also known as format strings. Read more about the format string syntax [here](https://docs.python.org/3/library/string.html#format-string-syntax).
