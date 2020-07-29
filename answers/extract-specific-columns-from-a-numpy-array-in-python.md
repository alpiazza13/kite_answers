headers:
    use-indexing: Use indexing
---
# How to extract specific columns from a NumPy array in Python
Extracting specific columns from a NumPy array gets a new array with only those columns.

## Use NumPy array indexing to extract specific colums {#use-indexing}

Use the syntax `array[:, [i, j]]` to extract the `i` and `j` indexed columns from `array`. Like lists, NumPy arrays use zero-based indexes.
```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([[1, 2, 3],[4, 5, 6]])
first_and_third_column = an_array[:, [0, 2]]
print(first_and_third_column)
```
Or, use `array[:, i:j+1]` to extract the `i` through `j` indexed columns from `array`.
```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([[1, 2, 3],[4, 5, 6]])
second_and_third_column = an_array[:, 1:3]
print(second_and_third_column)
```
