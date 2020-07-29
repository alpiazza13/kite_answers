headers:
    use-pd.DataFrame.duplicated: Use `pd.DataFrame.duplicated()`
---
# How to extract all duplicate rows from a Pandas DataFrame in Python
Extracting all duplicate rows in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) gets all rows which have an identical copy in the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pd.DataFrame.duplicated()`](kite-sym:pandas.DataFrame.duplicated) to extract all duplicate rows {#use-pd.DataFrame.duplicated}
Call [`pd.DataFrame.duplicated()`](kite-sym:pandas.DataFrame.duplicated) to get `True` if a row in [`pd.DataFrame`](kite-sym:pandas.DataFrame) has a duplicate and `False` otherwise. Only one row in each set of identical rows gets a `True` value. Subset a [`DataFrame`](kite-sym:pandas.DataFrame) using this result to extract the duplicate rows.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "a", "a"], "Numbers": [1, 1, 1, 3]})
# gets duplicate rows
has_duplicate = a_dataframe.duplicated()
duplicates = a_dataframe[has_duplicate]

print(duplicates)
```
