headers:
    use-a-list-comprehension: Use a list comprehension
---
# How to extract a column from a multidimensional array in Python
Extracting a column from a multidimensional array gets an array with only the elements in that column.

## Use a list comprehension to extract a column from an array {#use-a-list-comprehension}
Use the syntax `[row[i] for row in array]` to extract the `i` - indexed column from `array`.
```python
an_array = [[1,2,3],
            [4,5,6],
            [7,8,9]]
column_one = [row[1] for row in an_array]
print(column_one)
```
**Further reading:** A list comprehension is often useful for extracting elements from a list. You can read more about list comprehensions [here](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python).
## Other solutions

Use [NumPy array indexing](https://numpy.org/devdocs/user/basics.indexing.html) to extract a column.
- NumPy arrays are built in multidimensional arrays, and so this solution is easier to implement. However, it requires importing the NumPy library.
