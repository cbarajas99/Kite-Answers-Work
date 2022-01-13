headers:
  use-bin: Use `bin()`
---
# How to convert a signed integer to a unsigned integer in Python
Signed integers and unsigned in integers are represented using two's complement, which uses binary numbers. Signed integers, like -4, have the same two's complement representation as the unsigned integer (-4 + (2**32)).

## Use [`bin()`](kite-sym:builtins.bin) to convert a signed integer to unsigned integer {#use-bin}
Convert the signed integer into its two's complement integer by adding (2**32) to the signed integer. Use [`bin()`](kite-sym:builtins.bin) to convert the two's complement integer into 32-bit binary form.
```python
signed_int = -4
two_complements = signed_int + (2 ** 32)
print(bin(two_complements))
```
