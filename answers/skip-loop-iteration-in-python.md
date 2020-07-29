headers:
    use-continue: Use `continue`
---
# How to skip a loop iteration in Python
If the current iteration of a loop is skipped, the loop will immediately move onto its next iteration.

## Use [`continue`](kite-sym:builtins.continue) to skip an iteration {#use-continue}
Call [`continue`](kite-sym:builtins.continue), which immediately moves a loop onto next its next iteration, to skip the desired iteration. In the code  below, [`continue`](kite-sym:builtins.continue) is executed if `number` is `3`, and so `3` is never printed.
```python
numbers = [1,2,3,4,5]
for number in numbers:
    if number == 3:
        continue
    else:
        print(number)
```
#539
https://stackoverflow.com/questions/549674
