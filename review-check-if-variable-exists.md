headers:
  check-local-global: Check if global or local
---
# How to check if a variable exists in Python
If a variable exists, then it is defined either locally or globally. A local variable is defined inside a function, while a global variable is defined outside a function.

## Check if a variable exists locally or globally {#check-local-global}
Use [`locals()`](kite-sym:builtins.locals) to return a dictionary of variables defined locally. Use the syntax `variable in locals()` to check if a variable is defined locally.
```python
def f():
    a_variable = 0
    # checks if a_variable is a local variable
    is_local = "a_variable" in locals()
    print(is_local)

f()
```
Use [`globals()`](kite-sym:builtins.globals) to return a dictionary for variables defined globally.
```python
def f():
    a_variable = 0
    # checks if a_variable is a global variable
    is_global = "a_variable" in globals()
    print(is_global)

f()

```

> **Further reading:**
> Read more about global and local variables [here](https://pythonprogramming.net/global-local-variables/)
