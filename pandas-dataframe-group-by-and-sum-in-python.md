headers:
    use-pd.groupby-and-pd.sum: Use `pd.groupby()` and `pd.sum()`
---
# How to group a Pandas DataFrame by column names and sum over each group in Python
Grouping a [DataFrame](kite-sym:pandas.core.frame.DataFrame) by multiple columns and summing over each group creates a new DataFrame with one row for each group and calculates the sum per group of all columns which don't define the groups.

## Use [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) and [`pd.sum()`](kite-sym:pandas.core.frame.DataFrame.sum) group and sum the DataFrame  {#use-pd.groupby-and-pd.sum}

Call [`dataframe.groupby(columns)`](kite-sym:pandas.core.frame.DataFrame.groupby) with `columns` as a list of columns by which to group. Then, call [`sum()`](kite-sym:pandas.core.frame.DataFrame.sum) on this result to compute the sum of the other columns in each group.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 10, 5], "Letter": ["a", "b", "a", "c"]})
grouped_dataframe = a_dataframe.groupby(["Name", "Letter"])
grouped_and_summed = grouped_dataframe.sum()
print(grouped_and_summed.reset_index())
```
