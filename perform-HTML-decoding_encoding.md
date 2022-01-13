headers:
  use-unescape-escape: Use `html.unescape()` and `html.escape()`
---
# How to perform HTML decoding and encoding in Python
Performing HTML decoding on a string results in the string with the original HTML-reserved characters. For example, decoding `"&lt;body&gt;"` results in `<body>`. Performing HTML encoding on a string results in the string with the HTML-reserved characters being replaced. For example, encoding `"<body>"` results in `"&lt;body&gt;"`.

## Use [`html.unescape()`](kite-sym:html.unescape) to perform HTML decoding and [`html.escape()`](kite-sym:html.escape) to perform HTML encoding {#use-unescape-escape}
Call [`html.unescape(s)`](kite-sym:html.unescape) with `s` as the string to decode it with original HTML-reserved characters. Call [`html.escape(s)`](kite-sym:html.escape) with `s` as the string to encode it by replacing HTML-reserved characters.
```python
import html

a_string = "&lt;body&gt;"
decoded_string = html.unescape(a_string)

print(decoded_string)

a_string = "<body>"
encoded_string = html.escape(a_string)

print(encoded_string)
```
