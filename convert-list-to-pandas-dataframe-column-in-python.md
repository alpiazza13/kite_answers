headers:
    use-DataFrame-initialization-or-indexing: Use DataFrame initialization or indexing
---
# How to use a list as a Pandas DataFrame column in Python
Using a list as a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) column  either creates a [`DataFrame`](kite-sym:pandas.DataFrame) from a list or adds a list as a column to an existing [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`DataFrame`](kite-sym:pandas.DataFrame) initilization or indexing to use a list as a column {#use-DataFrame-initialization-or-indexing}

Use [`pandas.DataFrame(data)`](kite-sym:pandas.DataFrame) with `data` as a dictionary with its key as a column name and its value as a list to create a [`DataFrame`](kite-sym:pandas.DataFrame) from a list. Use the syntax `column = list` with `column` as a new column to add `list` to a [`DataFrame`](kite-sym:pandas.DataFrame).
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
numbers = [1, 2, 3]
# create `df` from `numbers`
df = pd.DataFrame({'Numbers': numbers})
print(df)


letters = ["a", "b", "c"]
# add `letters` to `df`
df["Letters"] = letters
print(df)
```
