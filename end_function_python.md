
headers:
    revert-indentation: Revert indentation
---
# How to end a function in Python
A function in python begins with the keyword `def`. Code written after the end of the function will not be ran when the function is called.

## Revert the indentation to end the function {#revert-indentation}
The body of a function starts at one further "unit" of indentation (one more press of the tab key) than its definition. To end a function, write a line of code with the same level of indentation as the function definition. In the code below, `x` evaluates to `0` instead of `1`, because the `print` call is not in the function.
```python
x = 0
def my_function():
    x = 1
print(x)
```
> **Further reading:**
> You can read about the many other uses of indentation in python   [here](https://docs.python.org/2.0/ref/indentation.html).
