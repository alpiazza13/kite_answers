headers:
    use-map-and-tuple: Use `map()` and `tuple()`
---
# How to convert a NumPy array to a tuple in Python
Converting a [NumPy array](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.html) to a tuple constructs a tuple consisting of one tuple for each row in an array.

## Use [map()](kite-sym:builtins.map) and [tuple()](kite-sym:builtins.tuple)to convert an array to a tuple {#use-map-and-tuple}
Call [`map(tuple, array)`](kite-sym:builtins.map) to convert each row in `array`, the original NumPy array, to a tuple. Then, convert this result into a tuple of tuples with [`tuple()`](kite-sym:builtins.tuple).

```python
KITE.start_prelude()
import numpy as np
KITE.stop_prelude()
an_array = np.array(((1, 2),(3, 4)))
array_of_tuples = map(tuple, an_array)
tuple_of_tuples = tuple(array_of_tuples)
print(tuple_of_tuples)
```
