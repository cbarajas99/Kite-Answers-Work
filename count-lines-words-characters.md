headers:
  use-split: Use `str.split()``
---
# How to count the lines, word, and characters within a text file in Python
Counting the lines, word, and characters within a text file results in the line count, word count, and character count, which includes spaces. For instance the text file containing `"Hello World\nHello Again\nGoodbye"` results on `lines: 3 words: 5 characters: 29`

## Use [`str.split()`](kite-sym:builtins.str.split) to count the lines, word, and characters within a text file {#use-split}
Call [`open(file, mode)`](kite-sym:builtins.open) with the pathname of a file as `file` and `mode` as `"r"` to open the file for reading. Use a for-loop to iterate through the file. At each iteration, use [`str.strip()`](kite-sym:builtins.str.strip) with `"\n"` as `characters` to strip it from each line `str`, and use [`str.split()`](kite-sym:builtins.str.split) to create a list containing all the words from the line `str`. Also, in each iteration, add 1 to the number of lines, use [`len(object)`](kite-sym:builtins.len) with the list containing the word from the line as `object` to add it to the number of words, and use [`len(object)`](kite-sym:builtins.len) with the stripped line as `object` to add it to the number of characters.
```python
KITE.set_display_code(False)
text = "Hello World\nHello Again\nGoodbye"
KITE.write_file('sample.txt',text)
KITE.display_file("sample.txt")
KITE.set_display_code(True)

file = open("sample.txt", "r")

number_of_lines = 0
number_of_words = 0
number_of_characters = 0
for line in file:
  # won't count \n as character
  line = line.strip("\n")
  words = line.split()
  number_of_lines += 1
  number_of_words += len(words)
  number_of_characters += len(line)

file.close()

print("lines:", number_of_lines, "words:", number_of_words, "characters:", number_of_characters)
```
