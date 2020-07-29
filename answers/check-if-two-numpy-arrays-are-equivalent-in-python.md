headers:
    use-all: Use `all()``
---
# How to check if two NumPy arrays are equivalent in Python
Checking if two [NumPy arrays](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.html) are equivalent determines whether every index of the two arrays are the same.

## Use [all()](kite-sym:builtins.all) to check if two arrays are equivalent {#use-all}
Call [`(array1 == array2).all()`](kite-sym:builtins.map) to return `True` if each element in `array1` is equal to its corrersponding element in `array2`, and `False` otherwise.

```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([[1,2],[3,4]])
another_array = np.array([[1,2],[3,4]])
equal_arrays = (an_array == another_array).all()
print(equal_arrays)
```
