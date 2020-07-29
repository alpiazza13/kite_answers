headers:
    use-str.join-and-str.ljust: Use `str.join()` and `str.ljust()`
---
# How to create nice column output in Python
Creating a nice column output from a list of lists representing a table creates output that resembles a table, with rows as each list within the list.

## Use [`str.join()`](kite-sym:builtins.str.join) and [`str.ljust()`](kite-sym:builtins.str.ljust) to create a column output {#use-str.join-and-str.ljust}
Use `max(len(entry) for row in table for entry in row)` to find the length of the longest `entry` in any `row` in `table`. Then, in a for loop that iterates over each element of the nested list (each `row` of `table`), use `print("".join(entry).ljust(column_with + padding) for entry in row)` to print each row with column lengths of `column_with + padding`, where `padding` is the number of blank spaces between each column in the outputted table and `column_with` is the value computed in the first step.
```python
a_table = [['ID', 'Name', 'Age'], ['1', 'John', '35'], ['2', 'Joseph', '40']]
column_width = max(len(entry) for row in a_table for entry in row)
for row in a_table:
    print ("".join(entry.ljust(column_width + 2) for entry in row))
```
