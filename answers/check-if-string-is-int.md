headers:
    use-str.isdigit-and-str.startswith: Use `str.isdigit()` and `str.startswith()`
---
# How to check if a string represents an integer in Python
A string represents an integer if it would be a valid integer if the enclosing `""` was removed. For example, `"1"` represents an integer, while `"1.5"` and `"1a"` do not.

## Use [`str.isdigit()`](kite-sym:builtins.str.isdigit) and [`str.startswith()`](kite-sym:builtins.str.startswith) to determine if the string represents an integer {#use-str.isdigit-and-str.startswith}
If `my_string.isdigit()` returns `True`, then `my_string` represents an integer because  `s.isdigit()` returns `True` if `s` consists solely of digits (0,1,...,9), and `False` otherwise. However, the string could also represent a negative integer, in which case `my_string.startswith("-")` and `my_string[1:].isdigit()` will return `True`.

```python
my_string = "-1"
is_positive_integer = my_string.isdigit()
is_negative_integer =  my_string.startswith("-") and my_string[1:].isdigit()
is_integer = is_positive_integer or is_negative_integer
print(is_integer)
```
