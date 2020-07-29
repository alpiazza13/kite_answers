headers:
    use-dict.update: Use `dict.update()`
---
# How to update a dictionary in Python
Updating a dictionary inserts a new entry into the dicitionary or modifies an existing one. For example, updating `{"a": 1, "b": 2}` with `{"c": 3}` returns  `{"a": 1, "b": 2, "c": 3}`.

## Use [`dict.update()`](kite-sym:builtins.dict.update) to update a dictionary {#use-dict.update}
Call  [`update(other_dictionary)`](kite-sym:builtins.dict.update), where `other_dictionary` contains the new entries to the dictionary. If a key `k` in `other_dictionary` already exists in the original dictionary, [`update`](kite-sym:builtins.dict.update) replaces the value associated with `k` with the one from `other_dictionary`.
```python
a_dictionary = {"a": 1, "b": 2}
a_dictionary.update({"a": 0, "c": 3})
print(a_dictionary)
```
Or, call `update(iterable)`, with `iterable` as a sequence of `key = value` assignments.
```python
a_dictionary = {"a": 1, "b": 2}
a_dictionary.update(a = 0, c = 3)
print(a_dictionary)
```
closes #960
https://stackoverflow.com/questions/17547507
