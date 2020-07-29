headers:
    call-function-with-another-function-as-input: Call function with another function as input
---
# How to pass a function as an argument of another function in Python
A Python function can take another function as an input, allowing that function to perform many different tasks. For example, a single function can, depending on its parameters, add two numbers, append an item to a list, and much more.

## Call the function with the name of another function as one of its arguments {#call-function-with-another-function-as-input}
Define `combine` such that it takes another function as an argument and uses that function to perform a task. Then, call `combine` with the name of the desired function as the first argument, ensuring that the second and third arguments are valid inputs to the first argument. Notice that `combine's` `function` parameter can be any function which takes two parameters.
```python
def add(a, b):
    return a + b
def appends(a_list, item):
    a_list.append(item)
    return a_list
def combine(function, a, b):
    return function(a,b)
sum = combine(add, 1, 2)
print(sum)
longer_list = combine(appends, [1,2], 3)
print(longer_list)
```
