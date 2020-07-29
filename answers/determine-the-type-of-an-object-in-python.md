headers:
    use-type: Use `type()`
---
# How to determine the type of an object in Python
Every object in Python belongs to a type. For example, the type of `[1,2,3]` is `list` and the type of `1` is `int`.

## Use [`type()`](kite-sym:builtins.type) to determine the type of an object {#use-type}
Call [`type()`](kite-sym:builtins.type) on the object in question.
```python
object = 1
type_of_object = type(object)
print(type_of_object)
```
