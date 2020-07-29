headers:
    use-next: Use `next()`
---
# How to search for a specific value in a list of dictionaries in Python
Given a list of dictionaries, each of which consists of multiple `(key,value)` pairs, searching for a specific value will return the dictionary in the list which contains that value.

## Use [`next()`](kite-sym:builtins.next) to search the list {#use-next}
In `dicts` below, to retrieve the dictionary which contains the `"Mary"`, use a for loop to iterate through `dicts` and find the dictionary whose `"name"` key corresponds to the value `"Mary"`. `next` returns the next item in an iterator. In this case, the iterator is a for loop, and, because of the if statement, `next` will not execute until the loop arrives at Mary's dictionary.
```python
dicts = [{"id":1, "name": "Alex"}, {"id":2, "name":"Joe"}, {"id":3, "name":"Mary"}]
mary_dict = next(dict for dict in dicts if dict["name"] == "Mary")
print(mary_dict)
```
