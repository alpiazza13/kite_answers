headers:
    use-pd.DataFrame.astype: Use `pd.DataFrame.astype()`
---
# How to convert the type of a Pandas DataFrame column from integer to string in Python
Converting the type of a [`DataFrame`](kite-sym:pandas.DataFrame) column to string converts each element in a columna to a string.

## Use [`pd.DataFrame.astype()`](kite-sym:pandas.DataFrame.astype) to convert a DataFrame column type from integer to string {#use-pd.DataFrame.astype}
Use [`column.astype(dtype)`](kite-sym:pandas.DataFrame.astype) with `dtype` as `str` and `column` as a column indexed from a DataFrame to convert the datatype of `column` from integer to string.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
a_dataframe["Numbers"] = a_dataframe["Numbers"].astype(str)
print(a_dataframe.dtypes)
```
