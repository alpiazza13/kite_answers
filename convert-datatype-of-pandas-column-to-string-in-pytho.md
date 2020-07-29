headers:
    use-pd.DataFrame.astype: Use `pd.DataFrame.astype()`
---
# How to convert the type of Pandas DataFrame columns to string in Python
Converting the type of [`DataFrame`](kite-sym:pandas.DataFrame) columns to string converts each element in some columns to a string.

## Use [`pd.DataFrame.astype()`](kite-sym:pandas.DataFrame.astype) to convert DataFrame column types to string {#use-pd.DataFrame.astype}
Use the indexing syntax `pd.DataFrame[[column_1, column_2]]` to extract `column_1` and `column_2` from `pd.DataFrame`. Call [`columns.astype(str)`](kite-sym:pandas.DataFrame.astype) to convert each element in `columns`, the resulting DataFrame from the previous extraction, to a string.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [0, 1, 2], "Integers": [1, 2, 3], "Floats": [1.0, 2.0, 3.0]})
a_dataframe[["Integers", "Floats"]] = a_dataframe[["Integers", "Floats"]].astype(str)
print(a_dataframe.dtypes)
```
