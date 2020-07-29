headers:
    use-DataFrame-indexing: Use DataFrame indexing
---
# How to subset a Pandas DataFrame in Python
Subsetting a [`DataFrame`](kite-sym:pandas.DataFrame) results in a new DataFrame with only the rows which satisfy a certain condition.

## Use DataFrame indexing to subset a DataFrame  {#use-DataFrame-indexing}
Use `pd.DataFrame[condition]`, with `condition` as a boolean expression involving `pd.DataFrame`, to select only the rows of `pd.DataFrame` which satisfy `condition`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
# Select rows where "Numbers" < 3
new_dataframe = a_dataframe[a_dataframe.Numbers < 3]
print(new_dataframe)
```
