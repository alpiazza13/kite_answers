headers:
    use-pd.reset_index: Use `pd.reset_index()`
---
# How to revert the indexing of a grouped Pandas DataFrame in Python
A grouped [DataFrame](kite-sym:pandas.core.frame.DataFrame)  results from using [`pd.groupby()`](kite-sym:pandas.core.frame.DataFrame.groupby)  with a mapping method on a DataFrame. This changes the indexing of the DataFrame, and reverting the index makes the DataFrame more readable and accessible.

## Use [`pd.reset_index()`](kite-sym:pandas.core.frame.DataFrame.reset_index) to revert the indexing  {#use-pd.reset_index}

Call [`dataframe.reset_index()`](kite-sym:pandas.core.frame.DataFrame.reset_index) with `dataframe` as a grouped DataFrame to reset the index.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Name': ['Alex', 'Jake', 'Alex', 'Jake'], 'Age': [10, 5, 20, 10]})
grouped_dataframe = a_dataframe.groupby('Name').sum()
reverted_index = grouped_dataframe.reset_index()
print(reverted_index)
```
