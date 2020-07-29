headers:
    use-pd.sort_values-and-pd.groupby: Use `pd.sort_values()` and `pd.groupby()`
---
# How to get sorted groups of a Pandas DataFrame in Python
Sorting the values in a grouped Pandas [DataFrame](kite-sym:pandas.core.frame.DataFrame) orders the values in each group in either ascending or descending order.

## Use [`pd.sort_values()`](kite-sym:pandas.core.frame.DataFrame.sort_values) and [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby) to get sorted groups of a DataFrame {#use-pd.sort_values-and-pd.groupby}
Call [`dataframe.sort_values(column, ascending=boolean)](kite-sym:pandas.core.frame.DataFrame.sort_values) to sort `dataframe` by `column` in ascending or descending order. Then, call [`groupby(column_two)`](kite-sym:pandas.core.frame.DataFrame.groupby) on this result to group by `column_two`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Name": ["Alex", "Jake", "Alex", "Jake"],
   "Age": [10, 5, 20, 10]})
sorted_dataframe = a_dataframe.sort_values("Age", ascending=False)
grouped_dataframe = sorted_dataframe.groupby("Name")
print(grouped_dataframe.get_group("Alex"))
```
