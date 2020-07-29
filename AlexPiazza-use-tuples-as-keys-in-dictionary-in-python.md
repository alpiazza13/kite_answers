headers:
    use-dictionary-syntax: Use dictionary syntax
---
# How to use tuples as keys in a dictionary in Python
A dictionary consists of keys through which values are accessed. These keys can be tuples.

## Use regular dictionary syntax to set tuples as keys in a dictionary {#use-dictionary-syntax}
Use the syntax `dictionary = {a_tuple: value1, another_tuple: value2}` to create a dictionary with keys as `a_tuple` and `another_tuple`. To access `value2`, use `dictionary[another_tuple]`.

```python
a_dictionary = {("Heads", "Heads"): 10, ("Heads", "Tails"): 11, ("Tails", "Tails"): 1}
two_head_flips = a_dictionary[("Heads", "Heads")]
print(two_head_flips)
```
