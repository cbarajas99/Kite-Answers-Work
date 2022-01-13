headers:
  use-equal-operator: Use `==`
  use-is: Use `is`
---
# How to compare two strings in Python
A string comparison checks whether two string objects are the same. String objects can be checked for equality or identity and will return a boolean to state whether two string objects are the same. For example, comparing `"abc"` and `"abc"` returns `True`.

## Use `==` to perform an equality comparison {#use-equal-operator}
Use the `==` operator to check if two string objects contain the same characters in order.
```python
string1 = "abc"
string2 = "".join(['a', 'b', 'c'])

# will result in boolean
is_equal = string1 == string2

print(is_equal)
```

## Use `is` to perform an identity comparison {#use-is}
Use the `is` keyword to check if two string objects are the same object.
```python
string1 = "abc"
string2 = "".join(['a', 'b', 'c'])

# will result in boolean
is_equal = string1 is string2

print(is_equal)
```

```python
string1 = "abc"
string2 =  string1

# will result in boolean
is_equal = string1 is string2

print(is_equal)
```
