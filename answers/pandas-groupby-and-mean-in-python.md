headers:
    use-pd.groupby-and-pd.mean: Use `pd.groupby()` and `pd.mean()`
---
# How to group a Pandas DataFrame by a column and compute the mean of each group in Python
Grouping a [DataFrame](kite-sym:pandas.core.frame.DataFrame) by a column and computing the mean of each group creates a new DataFrame with one row for each group and for each group calculates an average of the columns which don't define the groups.

## Use [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) and [`pd.mean()`](kite-sym:pandas.core.frame.DataFrame.mean) to compute averages by groups  {#use-pd.groupby-and-pd.mean}

Call [`dataframe.groupby(column)`](kite-sym:pandas.core.frame.DataFrame.groupby) with `column` as the column by which to group. Then, call [`mean()`](kite-sym:pandas.core.frame.DataFrame.mean) on this result to compute the mean of the other columns in each group.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 20, 10]})
grouped_dataframe = a_dataframe.groupby("Name")
with_means = grouped_dataframe.mean()
print(with_means.reset_index())
```
