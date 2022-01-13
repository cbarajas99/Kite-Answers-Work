headers:
  use-encode: Use `str.encode()`
---
# How to remove non-ASCII characters in Python
Removing non-ASCII characters results in a string that only contains ASCII characters. For example, removing non-ASCII characters from `"àa string withé fuünny charactersß"` results in `"a string with funny characters"`.

## Use [`str.encode()`](kite-sym:builtins.str.encode) to remove non-ASCII characters {#use-printable}
Call [`str.encode(encoding, errors)`](kite-sym:builtins.str.encode) with `encoding` as `"ASCII"` and `errors` as `"ignore"` to return `str` without `"ASCII"` characters.  Use [`str.decode()`](kite-sym:builtins.str.decode) to encode `str`.

```python
string_with_nonASCII = "àa string withé fuünny charactersß."

encoded_string = string_with_nonASCII.encode("ascii", "ignore")
decode_string = encoded_string.decode()

print(decode_string)
```
