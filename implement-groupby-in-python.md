headers:
    use-dict.update-and-list.append: Use `dict.update()` and `list.append()`
---
# How to implement a group by in Python
Implementing a group by converts a list of tuples into a dictionary or list displaying groups.

## Use [`dict.update()`](kite-sym:builtins.dict.update) and [`list.append()`](kite-sym:builtins.list.append) to implement a group by {#use-dict.update-and-list.append}
First, define an empty dictionary `groups`. Then, use a for-loop to iterate over all `group, value` pairs in a list. If the current `group` isn't in `groups`, call [`d1.update(d2)`](kite-sym:builtins.dict.update) with `d1` as `groups` and `d2` as a dictionary containing the key `group` mapped to a list containing `value`. Otherwise, use [`append()`](kite-sym:builtins.list.append) to add `value` to the current group in `groups`.
```python
data = [ ("integer", 1), ("string", "a"), ("float", 1.0), ("integer", 2), ("float", 2.0), ("string", "b")]
groups = {}
for group, value in data:
    if group not in groups:
        groups.update({group: [value]})
    else:
        groups[group].append(value)
print(groups)
```
If the output must be a list rather than a dictionary, start with the same code as above. Then, use a list comprehension which loops over [`groups.items()`](kite-sym:builtins.dict.items) to create a list representation of `groups`.
```python
data = [ ("integer", 1), ("string", "a"), ("float", 1.0), ("integer", 2), ("float", 2.0), ("string", "b")]
groups = {}
for group, value in data:
    if group not in groups:
        groups.update({group: [value]})
    else:
        groups[group].append(value)
groups_list = [(key, value) for key, value in groups.items()]
print(groups_list)
```

## Other solutions
Use [`itertools.groupby()`](kite-sym:itertools.groupby) to implement a group by. This solution is simpler to implement, but requires importing the [Itertools](https://docs.python.org/2/library/itertools.html) library.
