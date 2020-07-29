headers:
    use-pandas.DataFrame.fillna: Use `pandas.DataFrame.fillna()`
---
# How to replace NaN values with zeros in a column of a pandas DataFrame in Python
Replacing NaN values with zeros in a column of a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) fills any missing values in the column with `0`.

## Use [`pandas.DataFrame.fillna()`](kite-sym:pandas.DataFrame.fillna) to replace NaN values with zeros in a column {#use-pandas.DataFrame.fillna}
Use the syntax `df[name]` to select the column named `name` from the [`DataFrame`](kite-sym:pandas.DataFrame) `df`. Call [`pandas.DataFrame.fillna(value)`](kite-sym:pandas.DataFrame.fillna) with `value` as `0` and `pandas.DataFrame` as the desired column to replace each `NaN` in `pandas.DataFrame` with `value`.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, 2, 3], "B": [4, 5, np.NaN]})
KITE.set_display_code(True)
print(df)

df["A"] = df["A"].fillna(0)

print(df)
```
