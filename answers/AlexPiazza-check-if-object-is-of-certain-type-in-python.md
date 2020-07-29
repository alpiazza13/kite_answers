headers:
    use-isinstance: Use `isinstance()`
---
# How to check if a variable is a certain type in Python
Checking if a variable is a certain type returns `True` if a variable belongs to a specified type, and `False` otherwise.

## Use [`isinstance()`](kite-sym:builtins.isinstance) to check if a variable is a certain type {#use-isinstance}
Call `isinstance(variable, type)` to check if `variable` is an instance of the class `type`.
```python
an_integer = 1
is_integer = isinstance(an_integer, int)
print(is_integer)
```
