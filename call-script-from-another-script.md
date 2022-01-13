headers:
  use-exec: Use `exec()`
---
# How to call a script from another script in Python
Calling a script from another script executes the script without having to physically opening the script and running it.

## Use [`exec()`](kite-sym:builtins.exec) to call a script from another script {#use-exec}
Call [`open(file)`](kite-sym:builtins.open) with `file` as the script to return a stream. Use [`file.read()`](kite-sym:builtins.file.read) with the stream as `file` to read it. Call [`exec(source)`](kite-sym:builtins.exec) with the read file as `source` to run the script.

```python
KITE.set_display_code(False)
KITE.write_file("hello.py", 'print("Hello")')
KITE.display_file("hello.py")
KITE.set_display_code(True)

stream = open("hello.py")
read_file = stream.read()
exec(read_file)
```
