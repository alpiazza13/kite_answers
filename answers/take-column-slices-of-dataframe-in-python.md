headers:
    loc: Use `pandas.DataFrame.loc`
    iloc: Use `pandas.DataFrame.iloc`
---
# How to take column slices of a Pandas DataFrame in Python
Taking column slices of a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) results in a new [`DataFrame`](kite-sym:pandas.DataFrame) containing only specified columns from the original [`DataFrame`](kite-sym:pandas.DataFrame).


## Use [`pandas.DataFrame.loc`](kite-sym:pandas.DataFrame.loc) to take column slices {#loc}
Use [`pandas.DataFrame.loc`](kite-sym:pandas.DataFrame.loc) with the indexing syntax `[:, fiist:last:step]` with `first` as the name of the first column to take, `last` as the name of the last column to take, and `step` as the number of indices to advance after each extraction. Or, use the syntax `[:, [columns]]` with `columns` as a list of column names to take.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"a": [1], "b": [2], "c": [3], "d": [4], "e": [5]})

df2 = df.loc[:, "a":"d":2]
print(df2)

df3 = df.loc[:, ["a", "d", "e"]]
print(df3)
```

## Use [`pandas.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) to take column slices {#iloc}
Use [`pandas.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) with the indexing syntax `[:, start:stop:step]` with `start` as the index of the first column to take, `stop` as the index of the last column to take, and `step` as the number of indices to advance after each extraction. Or, use the syntax `[:, [indices]]` with `indices` as a list of column indices to take.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"a": [1], "b": [2], "c": [3], "d": [4], "e": [5]})

df2 = df.iloc[:, 0:3:2]
print(df2)

df3 = df.iloc[:, [0, 3, 4]]
print(df3)
```
