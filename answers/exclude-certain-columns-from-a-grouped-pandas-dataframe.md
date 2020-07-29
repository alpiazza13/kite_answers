headers:
    use-dataframe-indexing: Use DataFrame indexing
---
# How to apply a mapping function to only a certain column in a grouped Pandas DataFrame
Applying a mapping function on a [DataFrame](kite-sym:pandas.core.frame.DataFrame) will by default perform a combining operation on all the non-group defining columns for each group, but a specific column can also be selected.

## Use DataFrame indexing to select a specific column {#use-dataframe-indexing}

Call `dataframe.groupby(grouper)[column].mapper` with `grouper` as the name of the column by which to group, `column` as the column to be included, and `mapper` as a mapping function. Only `grouper` and `column` will be included in the new DataFrame.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1,2,3,4], "Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 10, 5]})
grouped_dataframe = a_dataframe.groupby("Name")["Age"].sum()
print(grouped_dataframe.reset_index())
```
