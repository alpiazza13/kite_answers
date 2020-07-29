headers:
    use-all: Use `all()`
---
# How to check if every element of a list satisfies a condition in Python
Each element in a list can be checked against a given condition. For example, checking whether each element in `[1,2,3]` is greater than 0 returns `True`.

## Use [`all()`](kite-sym:builtins.all) to check each element {#use-all}
Call [`all`](kite-sym:builtins.all)  using a for-loop to check each item in the list against a specified condition. [`all(iterable)`](kite-sym:builtins.all) returns `True` if each item in `iterable` evaluates to `True`, and `False` otherwise. In the code below, `iterable` is a generator object consisting of three `True`'s.
```python
numbers = [1,2,3]
all_greater_than_zero = all(number > 0 for number in numbers)
print(all_greater_than_zero)
```
