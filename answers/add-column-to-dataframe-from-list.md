headers:
    use-DataFrame-indexing: Use DataFrame indexing
---
# How to add a column to a Pandas DataFrame from a list in Python
Adding a column to a [`DataFrame`](kite-sym:pandas.DataFrame) from a list adds a new column to a DataFrame consisting of the elements in a given list.

## Use DataFrame indexing to add a column to a DataFrame from a list {#use-DataFrame-indexing}
Use the syntax `pd.DataFrame[column_name] = list` to add a column with name `column_name` and the same elements as those in `list` to `pd.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
a_list = ["Alex", "Jake", "John"]
a_dataframe["Names"] = a_list
print(a_dataframe)
```
