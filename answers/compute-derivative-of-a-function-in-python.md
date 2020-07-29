headers:
    use-sympy.Symbol: Use `sympy.Symbol()`
---
# How to find the derivative of a function in a Python.
Finding the derivative of a function computes its derivative with respect to a certain variable.

## Use [`sympy.Symbol()`](https://docs.sympy.org/latest/guide.html) find the derivative of a function {#use-sympy.Symbol}
Use [`sympy.Symbol("x")`](https://docs.sympy.org/latest/guide.html) to create a symbol object. Use this object to define a function, and call `function.diff(x)` to compute the derivative of `function` with respect to `x`.
```python
KITE.start_prelude()
import sympy
KITE.stop_prelude()
x = sympy.Symbol("x")
y = x**2 + 5*x + 5
derivative = y.diff(x)

print(derivative)
```
