headers:
    use-numpy.mean-and-numpy.std: Use `numpy.mean()` and `numpy.std`
---
# How to remove outliers from a Numpy array in Python.
Removing outliers from a NumPy [array](kite-sym:numpy.array) in Python results in a new array without any outliers.

## Use [`numpy.mean()`](kite-sym:numpy.mean) and [`numpy.std()`](kite-sym:numpy.std) to remove outliers from an array {#use-numpy.mean-and-numpy.std}
Find the mean and standard deviation of an array using [`np.mean(a)`](kite-sym:numpy.mean) and [`np.std(a)`](kite-sym:numpy.std), with `a` as an array. Get a new array with the distance from the mean of each element in an array using [`abs(a - mean)`](kite-sym:builtins.abs). Determine if a given element is not an outlier by checking if its distance from the mean is less than the standard deviation multiplied by a constant. The constant is the number of standard deviations away from the mean by which an outlier is defined. Subset the original array using this calculation to get a new array without any outliers.

```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array([1, 1, 1, 1, 1, 1, 10])
mean = np.mean(an_array)
standard_deviation = np.std(an_array)
distance_from_mean = abs(an_array - mean)
max_deviations = 2
not_outlier = distance_from_mean < max_deviations * standard_deviation
no_outliers = an_array[not_outlier]

print(no_outliers)
```
