headers:
    use-array-slicing: Use array slicing
---
# How to extract a column from a multidimesional array in Python

A multidimensional array takes the form of a [NumPy array](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.html). Extracting the second column from `[[1,2],[3,4]]` results in `[2 4]`.

## Use [NumPy array slicing](https://www.pythoninformer.com/python-libraries/numpy/index-and-slice/) to extract a column {#use-array-slicing}

Execute `an_array[:,column]` with `column` as the index of the column to extract. `:` indicates that every row will be included in the output.

```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([[1, 2],[3, 4]])
second_column = an_array[:,1]
print(second_column)
```
closes #679
https://stackoverflow.com/questions/903853
