headers:
    use-pd.DataFrame.apply: Use `pd.DataFrame.apply()`
---
# How to apply a function with multiple arguments to a Pandas DataFrame in Python
Applying a function with multiple arguments to a [`DataFrame`](kite-sym:pandas.DataFrame) changes the elements in the DataFrame using a given function.

## Use [`pd.DataFrame.apply()`](kite-sym:pandas.DataFrame.apply) to apply a function with multiple arguments to a column in a DataFrame  {#use-pd.DataFrame.apply}
Use `pd.DataFrame.apply(func, args=tuple)`, with `tuple` as a tuple specifying all arguments of `func`, a function, except the first one. The first argument of `func` will be the current element in `pd.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Numbers": [1, 2, 3]})
def subtract(x, y, z):
    return x - y - z
#number => number - 1 - 2
a_dataframe = a_dataframe.apply(subtract, args=(1,2))
print(a_dataframe)
```
