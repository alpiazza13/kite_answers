headers:
    use-pd.groupby-and-pd.max: Use `pd.groupby()` and `pd.max()`
---
# How to get the maximum values of each group in a Pandas DataFrame in Python
Getting the maximum values in a grouped Pandas [DataFrame](kite-sym:pandas.core.frame.DataFrame) displays the highest value of each column in each group.

## Use [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) and [`pd.max()`](kite-sym:pandas.core.frame.DataFrame.max) to group a DataFrame and get the maximum values in each group {#use-pd.groupby-and-pd.max}

Call [`dataframe.groupby(column)`](kite-sym:pandas.core.frame.DataFrame.groupby) to group `dataframe` by `column`. Then, call [`max()`](kite-sym:pandas.core.frame.DataFrame.max) on this result to get the maximum values of the other columns in each group.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1,2,3,4], "Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [30, 10, 20, 5]})
grouped_dataframe = a_dataframe.groupby("Name")
maximums = grouped_dataframe.max()
print(maximums.reset_index())
```
