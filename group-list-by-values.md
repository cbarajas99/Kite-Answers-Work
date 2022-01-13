headers:
  use-list-comprehension: Use a list comprehension
---
# How to group a list by values in Python
Grouping a list by values converts a list of two-element lists into a list of lists grouped by the second element and containing only the first element in each original inner list. For example, grouping `[["A", 0], ["B", 1], ["C", 0], ["D", 2], ["E", 2]]` by its values results in `[["A", "C"], ["B"], ["D", "E"]]`.

## Use a list comprehension to group a list by values {#use-map}
Use the list comprehension syntax `[list[1] for list in list_of_lists]` to get a list containing only the second element from each `list` in `list_of_lists`. Call `set(list)` with `list` as the previous result to remove any duplicate elements from `list`. Create an empty `result` list and use a for-loop to iterate through `set`. At each iteration, create an empty list `group` and use another for-loop to iterate through the original `list_of_lists`. At each iteration of this loop, check if the second element of the current list in `list_of_lists` equals the current element in `set`. If it does, append this value to `group`. Outside the inner for-loop, append `group` to `result`.

```python
list_of_lists = [["A", 0], ["B", 1], ["C", 0], ["D", 2], ["E", 2]]

all_values = [list[1] for list in list_of_lists]
unique_values = set(all_values)

group_list = []
for value in unique_values:
  this_group = []
  for list in list_of_lists:
    if list[1] == value:
      this_group.append(list[0])
  group_list.append(this_group)

print(group_list)
```
Use a nested list comprehension for a more compact implementation.
```python
list_of_lists = [["A", 0], ["B", 1], ["C", 0], ["D", 2], ["E", 2]]

unique_values = set([list[1] for list in list_of_lists])
group_list = [[a_list[0] for a_list in list_of_lists if a_list[1] == value] for value in unique_values]

print(group_list)
```
