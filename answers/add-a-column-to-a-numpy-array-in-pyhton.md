headers:
    use-numpy.append: Use `numpy.append()`
---
# How to add a column to a NumPy array in Python
Adding a column to a NumPy array in Python updates the array with the values stored in the new column.

## Use [`numpy.append()`](kite-sym:numpy.append) to add a column to an array {#use-numpy.append}

Call [`np.append(array, new_column, axis = 1)`](kite-sym:numpy.append) to add `new_column` to `array`.
```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([[1, 2],[3, 4]])
new_column = [[5], [6]]
an_array = np.append(an_array, new_column, axis = 1)
print(an_array)
```
