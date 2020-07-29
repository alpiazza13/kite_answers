headers:
    use-for-loop: Use for-loop
---
# How to loop over a list in Python
Looping over a list passes over each element in the list, allowing something to be done with or asked about every element.

## Use a for-loop to loop over a list {#use-for-loop}
A for-loop passes over each item in a list. In the code below, `number` is a different element at each iteration, starting as `1` and ending as `3`.
```python
numbers = [1,2,3]
for number in numbers:
    print(number)
```

Or, use a while loop to do the same thing. A while loop is useful if not every element in the list has to be acted upon, as `i` can be incremented by any amount. It also keeps track of the current position in the list, assuming `i` starts at `0` and is incremented by one at each iteration.
```python
numbers = [1,2,3]
i = 0
while i < len(numbers):
    number = numbers[i]
    print(number)
    i = i + 1
```
#381
https://stackoverflow.com/questions/9138112
