headers:
  use-for: Use a for loop
---
# How to divide each element in a list in Python
Dividing each element in a list by a number results in a new list containing the quotients.

## Use a for loop to divide each element in a list {#use-for}
Use a for loop to iterate through each element in the list. Use the division operator (`/`) to divide by a number. Append the resultant quotients to a new list.

```python
numbers = [1, 2, 3]

quotients = []
for number in numbers:
    # divides each element by 2
    quotients.append(number / 2)

print(quotients)
```
Use a list comprehension for a more compact implementation
```python
numbers = [1, 2, 3]

# divides each element by 2
quotients = [number / 2 for number in numbers]

print(quotients)
```

> **Further reading:**
> List comprehensions provide a concise way to create lists to perform operations on. You can read more about list comprehensions [here](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions).
