headers:
    use-pd.groupby: Use `pd.groupby()`
---
# How to group a Pandas DataFrame by multiple columns in Python
Grouping a Pandas [DataFrame](kite-sym:pandas.core.frame.DataFrame) by columns `a` and `b` creates groups consisting of rows which have the same value in `a` and `b`.

## Use [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) to group a DataFrame by multiple columns {#use-pd.groupby}

Call [`dataframe.groupby(columns)`](kite-sym:pandas.core.frame.DataFrame.groupby) with `columns` as a list of the columns by which to group.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1,2,1,4], "Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 10, 5]})
grouped_dataframe = a_dataframe.groupby(["ID", "Name"])
print(grouped_dataframe.indices)
```
