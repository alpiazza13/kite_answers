headers:
    use-numpy.linalg.norm: Use `numpy.linalg.norm()`
---
# How to get the magnitude of a vector in Numpy in Python
Getting the magnitude of a NumPy [array](kite-sym:numpy.array) representing a vector computes the square root of the summation of each element squared. For example, the magnitude of `[3, 4]` is `25`.

## Use [`numpy.linalg.norm()`](kite-sym:numpy.linalg.norm) to get the magnitude of a vector {#use-numpy.linalg.norm}

Call [`numpy.linalg.norm(x)`](kite-sym:numpy.linalg.norm) with `x` as an [array](kite-sym:numpy.array) to compute the magintude of the vector respresented by `x`.
```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
vector = np.array([3, 4])

# compute magnitude of (3,4)
magnitude = np.linalg.norm(vector)
print(magnitude)
```
