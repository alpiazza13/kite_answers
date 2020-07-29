headers:
    use-any: Use `any()`
---
# How to check if a string contains an element from a list in Python
A string `a_string` contains an element from a list `a_list` of strings if some substring of `a_string` is an item in `a_list`. For example, `"abc@gmail.com"` contains an element from `["gmail", "hotmail", "yahoo"]`.

## Use [`any()`](kite-sym:builtins.any) to check if a string contains an element from a list {#use-any}
Call [`any`](kite-sym:builtins.any) with a generator expression to check if any item from the list is in the string. In the code below, since `"gmail"` is a substring of `user_email`, the loop computes `True` on its second iteration, and [`any`](kite-sym:builtins.any) returns `True`.
```python
user_email = "abc@gmail.com"
email_services = ["hotmail", "gmail", "yahoo"]
email_contains_service = any(email_service in user_email for email_service in email_services)
print(email_contains_service)
```
#372
https://stackoverflow.com/questions/6531482

A string `a_string` contains an element from a list `a_list` of strings if, for some `i`, `j`, `k`, `a_list[k] = a_string[i:j]`
