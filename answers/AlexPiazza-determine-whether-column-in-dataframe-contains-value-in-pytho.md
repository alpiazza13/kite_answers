headers:
    use-DataFrame-indexing: Use DataFrame indexing
---
# How to determine whether a column of a Pandas DataFrame contains a value
Determining whether a column of a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) contains a value returns `True` if that value is in a [`DataFrame`](kite-sym:pandas.DataFrame), and `False otherwise.`

## Use [`DataFrame`](kite-sym:pandas.DataFrame) indexing to determine whether a column contains a value {#use-DataFrame-indexing}
Use the syntax `value in pd.DataFrame[column]` with `column` as the name of the column in question to check if `value` is in `column`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
value_in_dataframe = 2 in a_dataframe["Numbers"]

print(value_in_dataframe)
```
