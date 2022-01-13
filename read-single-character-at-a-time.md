headers:
  use-nested-for-loop: Use a nested for loop
  use-file-read: Use `file.read()`
---
# How to read a file character by character in Python
Reading a file character by character accesses the characters in a file one at a time.

## Use a nested for loop to read file character by character {#use-nested-for-loop }
Use [`open(file, mode)`](kite-sym:builtins.open) with the filename as `file` and `"r"` as `mode`to open a file. Use a for loop to iterate through each line of the file. Use a nested for loop to iterate through each character of each line. Use [`file.close()`](kite-sym:builtins.file.close) with the filename as `file` to close the file.
```python
KITE.set_display_code(False)
text = "abcd"
KITE.write_file('sample.txt',text)
KITE.set_display_code(True)
file = open("sample.txt", "r")
for line in file:
    for character in line:
        print(character)
file.close()
```

## Use [`file.read()`](kite-sym:builtins.file.read) to read a file byte by byte {#use-file-read}
Use [`file.read(size)`](kite-sym:builtins.file.read) with `1` as `size` to read the next character in `file`.

```python
KITE.set_display_code(False)
text = "abcd"
KITE.write_file('sample.txt',text)
KITE.set_display_code(True)

file = open("sample.txt", "r")
first_character = file.read(1)
print(first_character)
second_character = file.read(1)
print(second_character)
file.close()
```
