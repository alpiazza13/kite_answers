
headers:
    use-pd.Series.idxmax: Use `pd.Series.idxmax()`
---
# How to find the row in a Pandas DataFrame with the maximum value for a column in Python
Finding the row in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) with the maximum value for a column results in the the row which has the largest element in a specified column.

## Use [`pd.Series.idxmax()`](kite-sym:pandas.Series.idxmax) to find the row with the maximum value for a column  {#use-pd.Series.idxmax}
Call [`pd.Series.idxmax()`](kite-sym:pandas.Series.idxmax) with [`pd.Series`](kite-sym:pandas.Series) as a column in a [DataFrame](kite-sym:pandas.DataFrame) to find the index of the maximum value in that column. Then, use [`pd.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) to extract the row with that position.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 4, 3]})
max_index = a_dataframe["Numbers"].idxmax()
max_row = a_dataframe.iloc[[max_index]]

print(max_row)
```
