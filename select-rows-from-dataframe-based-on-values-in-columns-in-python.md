headers:
    use-DataFrame-indexing: Use DataFrame indexing
---
# How to select rows from a Pandas DataFrame based on values in a column in Python
Selecting rows from a [`DataFrame`](kite-sym:pandas.DataFrame) based on values in a column results in a new DataFrame with only the rows which satisfy specified conditions.

## Use DataFrame indexing to selct rows from a DataFrame based on column values {#use-DataFrame-indexing}
Use the indexing syntax `pd.DataFrame[(condition_1) & (condition_2)]`, with `condition_1` and `condition_2` as boolean expressions, to select only the rows which statisfy both conditions.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Numbers": [1, 2, 3], "Letters": ["a", "b", "c"]})
condition_one = a_dataframe["Numbers"] < 3
condition_two = a_dataframe["Numbers"] % 2 == 1
#only odd numbers less than three
new_dataframe = a_dataframe[condition_one & condition_two]
print(new_dataframe)
```
