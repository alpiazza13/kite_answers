headers:
    use-a-for-loop: Use a for-loop
---
# How to unpack each tuple in a list in Python
Unpacking a tuple gives access to each element in the tuple as a variable. For example, unpacking `(1, 2)` assigns `1` and `2` their own variables.

## Use a for-loop to unpack each tuple in a list {#use-a-for-loop}
Use the syntax `for a, b in list` to unpack every `(a,b)` tuple in a list.

```python
list_of_tuples = [("a", "b"), ("c", "d"), ("e", "f")]
for first_element, second_element in list_of_tuples:
    print("This tuple contains", first_element, "and", second_element)
```
