headers:
    use-a-for-loop: Use a for-loop
---
# How to use itertools.groupby in Python
`itertools.groupby` provides iterative access to each group key and its associated key-value pairs.

## Use a for-loop to iterate through the result of [`itertools.groupby()`](kite-sym:itertools.groupby) {#use-a-for-loop]
Use the syntax [`for key, group in itertools.groupby(l, key_f)`](kite-sym:itertools.groupby) with `l` as a list to be grouped and `key_f` as a function which maps each element of `l` to its value which will define a group. Each `key` is a name of a group and each `group` is a list of `key, value` pairs. Note that [`groupby`](kite-sym:itertools.groupby) only works if `l` is already sorted by its groups.
```python
KITE.start_prelude()
import itertools
KITE.stop_prelude()
data = [("integer", 1), ("integer", 2), ("string", "a"), ("string", "b"), ("float", 1.0), ("float", 2.0)]
for key, group in itertools.groupby(data, lambda x : x[0]):
    key_and_group = {key : list(group)}
    print(key_and_group)
```
