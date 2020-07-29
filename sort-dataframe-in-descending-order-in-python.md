headers:
    use-pd.sort_values: Use `pd.sort_values()`
---
# How to sort a Pandas DataFrame in descending order in Python
Sorting a [DataFrame](kite-sym:pandas.core.frame.DataFrame) in descending order organizes a DataFrame's rows from highest to lowest value of a certain column.
## Use [`pd.sort_values()`](kite-sym:pandas.core.frame.DataFrame.sort_values) to sort a DataFrame in descending order {#use-pd.sort_values}
Call [`dataframe.sort_values(column, ascending=False)`](kite-sym:pandas.core.frame.DataFrame.sort_values) to sort `dataframe` in descending order based on the values in `column`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [3, 2, 1], "Points": [10, 20, 30]})
sorted_dataframe = a_dataframe.sort_values(["Points"], ascending=False)
print(sorted_dataframe)
```
