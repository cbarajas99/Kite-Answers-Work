headers:
  use-exec: Use `exec()`
---
# How to run a script from a separate Python file in Python
Running a script from a separate file executes the script without having to physically open the file and run it.

## Use [`exec()`](kite-sym:builtins.exec) to run a script from IDLE interactive shell {#use-exec}
Call [`open(file)`](kite-sym:builtins.open) with a script as `file` to return a stream. Use [`file.read()`](kite-sym:builtins.file.read) with the stream as `file` to read it. Call [`exec(source)`](kite-sym:builtins.exec)  with the read file as `source` to run the script.
```python
KITE.set_display_code(False)
KITE.write_file("hello.py", 'print("Hello")')
KITE.set_display_code(True)

stream = open("hello.py")
read_file = stream.read()
exec(read_file)
```
