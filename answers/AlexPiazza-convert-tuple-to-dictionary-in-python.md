headers:
    use-dict: Use `dict()`
---
# How to convert a tuple to a dictionary in Python
Converting a tuple consisting of other tuples of length two creates a dictionary with keys as the one element in each tuple and values as the other element. For example, converting `((k1, v1), (k2, v2))` to a dictionary results in either `{k1: v1, k2: v2}` or `{v1: k1, v2: k2}`.

## Use [`dict()`](kite-sym:builtins.dict) to convert a tuple to a dictionary {#use-dict}
Call [`dict(tuple)`](kite-sym:builtins.dict) to create a dictionary with keys as the first elements in `tuple` and values as the second elements in `tuple`.

```python
a_tuple = ((1, "a"), (2, "b"))
tuple_as_dictionary = dict(a_tuple)
print(tuple_as_dictionary)
```
Call [`dict((a, b) for (b, a) in tuple)`](kite-sym:builtins.dict) to create a dictionary with keys as the second elements in `tuple` and values as the first elements in `tuple`.

```python
a_tuple = ((1, "a"), (2, "b"))
tuple_as_dictionary = dict((letter, number) for (number, letter) in a_tuple)
print(tuple_as_dictionary)
```
