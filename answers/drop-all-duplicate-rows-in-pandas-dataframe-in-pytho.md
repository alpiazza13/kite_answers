headers:
    use-pd.DataFrame.drop_duplicates: Use `pd.DataFrame.drop_duplicates()`
---
# How to drop all duplicate rows in a Pandas DataFrame in Python
Dropping all duplicate rows in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) removes all rows which have an identical copy in the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pd.DataFrame.drop_duplicates()`](kite-sym:pandas.DataFrame.drop_duplicates) to set a new column as the index {#use-pd.DataFrame.drop_duplicates}
Call [`pd.DataFrame.drop_duplicates(keep=False)`](kite-sym:pandas.DataFrame.drop_duplicates)a to remove all duplicate rows from [`pd.DataFrame`](kite-sym:pandas.DataFrame).
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "a", "a"], "Numbers": [1, 1, 1, 2]})
#remove duplicate rows
no_duplicates = a_dataframe.drop_duplicates(keep=False)

print(no_duplicates)
```
