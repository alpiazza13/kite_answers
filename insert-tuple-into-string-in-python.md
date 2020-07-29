headers:
    use-string-formatting: Use string formatting
---
# How to insert a tuple into a string in Python
Inserting a tuple into a string creates a string with an easily readable tuple in it.

## Use string formatting to insert a tuple into a string {#use-string-formatting}
Use the syntax `f"{tuple} in string"`, to get a string with `tuple` inserted at the specified position.

```python
a_tuple = (1, 2)
string_with_tuple = f"{a_tuple} is a tuple."
print(string_with_tuple)
```
> **Further reading:**
> You can read about other methods of string formatting [here](https://realpython.com/python-string-formatting/).
