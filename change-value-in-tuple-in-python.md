headers:
    use-list-and-tuple: Use `list()` and `tuple()`
---
# How to change a value in a tuple in Python
Because tuples are immutable, changing a value in a tuple creates a new tuple. For example, changing the `0` to `3` in `(0,1,2)` will create a new tuple, `(3,1,2)`.

## Use [`list()`](kite-sym:builtins.list) and [`tuple()`](kite-sym:builtins.tuple) to chnage the value. {#use-list-and-tuple}
Call [`list(iterable)`](kite-sym:builtins.list) to change `iterable` (the tuple, in this case) into a list. After changing the desired value in the new list, call [`tuple(iterable)`](kite-sym:builtins.tuple) to change `iterable` (in this case, the just-created list) into a `tuple`.
```python
a_tuple = (0,1,2)
a_list = list(a_tuple)
a_list[0] = 3
updated_a_tuple = tuple(a_list)
print(updated_a_tuple)
```

> **Further reading:**
> You can read more about mutable and immutable objects in python [here](https://www.geeksforgeeks.org/mutable-vs-immutable-objects-in-python/).

#554
https://stackoverflow.com/questions/11458239
