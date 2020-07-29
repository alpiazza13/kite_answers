headers:
    use-pd.groupby-and-pd.first: Use `pd.groupby()` and `pd.first()`
---
# How to get the first value of each group in a Pandas DataFrame in Python
Getting the first value in a grouped Pandas [DataFrame](kite-sym:pandas.core.frame.DataFrame) displays the row in each group which has the lowest index.

## Use [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) and [`pd.first()`](kite-sym:pandas.core.frame.DataFrame.first) to group a DataFrame and get the first value in each group {#use-pd.groupby-and-pd.first}

Call [`dataframe.groupby(column)`](kite-sym:pandas.core.frame.DataFrame.groupby) to group `dataframe` by `column`. Then, call [`first()`](kite-sym:pandas.core.frame.DataFrame.first) on this result to get the first value in each group.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 20, 10]})
grouped_dataframe = a_dataframe.groupby("Name")
first_values = grouped_dataframe.first()
print(first_values.reset_index())
```
