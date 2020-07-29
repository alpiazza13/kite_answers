headers:
    use-join: Use `join()`
---
# How to join a list of integers into a string in Python
Joining a list of integers into a string will convert the list into a
string of numbers. For example, `[1,2,3]` will turn into `"1, 2, 3"`.

## Use [`join()`](kite-sym:builtins.join) to construct the string {#use-join}
`join()` puts each item in an iterable into a string. A string to
separate each item, in this case `", "` must be specified when calling `join`,
and each item in the iterable must be a string. So, convert each item in `ints`
to a string using a for loop and [`str()`](kite-sym:builtins.str), and call `join` on this new list.
```python
ints = [1,2,3]
str_of_ints = ', '.join(str(int) for int in ints)
print(str_of_ints)
```
