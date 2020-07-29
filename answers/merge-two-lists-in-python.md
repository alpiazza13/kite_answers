headers:
    use-+: Use `+`
---
# How to merge lists together in Python
Merging lists creates a list containing all of the elements from every list. For example, merging `[1, 2]`, `[3, 4]`, and `[5, 6]` results in `[1, 2, 3, 4, 5, 6]`.

## Use `+` to merge two lists {#use-+}
Sum all the lists together to create a merged list.
```python
list_one = [1, 2]
list_two = [3, 4]
list_three = [5, 6]
merged_list = list_one + list_two + list_three
print(merged_list)
```

closes #246
https://stackoverflow.com/questions/3748063
wasnt entirely sure what to do, but interepreted it as merging
