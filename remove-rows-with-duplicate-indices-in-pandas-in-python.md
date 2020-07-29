headers:
    use-pd.DataFrame.duplicated: Use `pd.DataFrame.duplicated()`
---
# How to remove rows in a Pandas DataFrame with duplicate indices in Python
If an index is repeated in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame), removing rows with duplicate indices keeps only the first row with that index.

## Use [`pd.DataFrame.duplicated()`](kite-sym:pandas.DataFrame.duplicated) to remove rows with duplicate indices {#use-pd.DataFrame.duplicated}
Extract the index from a [`DataFrame`](kite-sym:pandas.DataFrame) using [`pd.DataFrame.index`](kite-sym:pandas.DataFrame.index). Call [`pd.DataFrame.duplicated(keep="first")`](kite-sym:pandas.DataFrame.duplicated) with the index as `pd.DataFrame` to get a series of booleans indicating whether each index has a duplicate in `pd.DataFrame`. Use `~` to reverse each entry in the series, then subset the original [`DataFrame`](kite-sym:pandas.DataFrame) using the boolean series to get a new [`DataFrame`](kite-sym:pandas.DataFrame) without any duplicate indices.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]}, index=[1, 1, 2])
index = a_dataframe.index
is_duplicate = index.duplicated(keep="first")
not_duplicate = ~is_duplicate
no_duplicate_indeces = a_dataframe[not_duplicate]

print(no_duplicate_indeces)
```
