headers:
    use-any: Use `any()`
---
# How to check if a list contains a substring in Python
A list contains a substring if any element in the list contains that substring. For example, `["one", "two", "three"]` contains `wo` because `wo` is a substring of `two`.

## Use [`any()`](kite-sym:builtins.any) to check if a list contains a substring {#use-any}
Call [`any`](kite-sym:builtins.any) with a for loop to check if the substring is in any element in the list.
```python
strings = ["one", "two", "three"]
substring = "wo"
substring_in_list = any(substring in string for string in strings)
print(substring_in_list)
```
Or, use a list comprehension to construct a list with every element in the list which contains the substring.
```python
strings = ["one", "two", "three"]
substring = "o"
strings_with_substring = [string for string in strings if substring in string]
print(strings_with_substring)
```
closes #247
https://stackoverflow.com/questions/4843158
