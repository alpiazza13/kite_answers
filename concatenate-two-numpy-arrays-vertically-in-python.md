headers:
    use-numpy.vstack: Use `numpy.vstack()`
---
# How to concatenate two NumPy arrays vertically in Python
Concatenating two NumPy [arrays](kite-sym:numpy.array) vertically creates a new array with each original array as a row.

## Use [`numpy.vstack()`](kite-sym:numpy.vstack) to concatenate two arrays vertically {#use-numpy.vstack}

Call [`np.vstack(array1, array2)`](kite-sym:numpy.vstack) to concatenate `array1` and `array2` vertically.
```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([1, 2])
another_array = np.array([3, 4])
stacked_array = np.vstack((an_array, another_array))

print(stacked_array)
```
