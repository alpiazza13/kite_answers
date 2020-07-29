headers:
    use-pd.DataFrame.get_loc: Use `pd.DataFrame.get_loc()`
---
# How to get the index of a Pandas DataFrame column from its name in Python
Given the name of a column in a [`DataFrame`](kite-sym:pandas.DataFrame), its index can be obtained.

## Use [`pd.DataFrame.get_loc()`](kite-sym:pandas.CategoricalIndex.get_loc) to get the index of a DataFrame column from its name {#use-pd.DataFrame.get_loc}
Use [`pd.DataFrame.columns`](kite-sym:pandas.DataFrame.columns) to obtain an object containing all column names in `pd.DataFrame`. On this result, call [`get_loc(key)`](kite-sym:pandas.CategoricalIndex.get_loc) with `key` as a column name, to get the index of `key`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
columns = a_dataframe.columns
letters_index = columns.get_loc("Letters")
print(letters_index)
```
