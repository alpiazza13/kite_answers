headers:
    use-DataFrame-indexing: Use DataFrame indexing
---
# How to add a column with a default value to a Pandas DataFrame in Python
Adding a column with a default value to a [`DataFrame`](kite-sym:pandas.DataFrame) adds a column to a DataFrame with each element as a specified value.

## Use DataFrame indexing to add a column with a default value to a DataFrame {#use-DataFrame-indexing}
Use the syntax `pd.Dataframe[new_column] = value` to add a column named `new_column` with each element as `value` to `pd.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
#add column of 0's
a_dataframe["Zero"] = 0
print(a_dataframe)
```
