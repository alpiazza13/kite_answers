headers:
    iloc: Use `pandas.DataFrame.iloc()`
---
# How to get the first column of a Pandas DataFrame as a Series in Python
Getting the first column of a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) as a [`Series`](kite-sym:pandas.Series) results in a Pandas [`Series`](kite-sym:pandas.Series) object representing the first column.


## Use [`pandas.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) to get the first column as a Series {#iloc}
Use [`pandas.DataFrame.iloc`](kite-sym:pandas.DataFrame.iloc) with the indexing syntax `[:, 0]` to access the first row of `pandas.DataFrame`. The result is a [`Series`](kite-sym:pandas.Series).

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})

first_column = df.iloc[:, 0]

print(first_column)
print(type(first_column))
```
