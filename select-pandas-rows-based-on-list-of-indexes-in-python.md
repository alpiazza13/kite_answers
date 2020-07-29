headers:
    use-pd.DataFrame.iloc: Use `pd.DataFrame.iloc()`
---
# How to select rows from a Pandas DataFrame based on a list of indexes in Python
Selecting rows from a [`DataFrame`](kite-sym:pandas.DataFrame)based on a list of indexes results in a new DataFrame with only the rows indicated by the list.

## Use [`pd.DataFrame.iloc()`](kite-sym:pandas.DataFrame.iloc) to select rows from a DataFrame  {#use-pd.DataFrame.iloc}

Call [`pd.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) to return an object containing the rows and columns of `pd.DataFrame`. Use the indexing syntax `object[list, :]` to extract the rows whose positions are in `list` from `object`. `:` indicates that every column will be included.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
list_of_indexes = [1,2]
rows = a_dataframe.iloc[list_of_indexes, :]
print(rows)
```
