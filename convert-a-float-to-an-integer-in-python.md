headers:
    use-int: Use `int()`
---
# How to convert a float to an integer in Python
Converting a float `a_float` to an integer changes `a_float` to the nearest whole number smaller than it. For example, converting `1.1` to an integer results in `1`.

## Use [`int()`](kite-sym:builtins.int) to convert a float to an integer {#use-int}
Call  [`int(float)`](kite-sym:builtins.int), to change `float` to an integer.
```python
a_float = 1.1
a_int = int(1.1)
print(a_int)
```
closes #637
https://stackoverflow.com/questions/3387655/safest-way-to-convert-float-to-integer-in-python

didn't see labeling
