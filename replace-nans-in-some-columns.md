headers:
    use-pandas.DataFrame.fillna: Use `pandas.DataFrame.fillna()`
---
# How to fill NaN values in only certain columns of a pandas DataFrame in Python
Filling NaN values in only certain columns of a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) replaces any missing values in the specified columns with a specified value.

## Use [`pandas.DataFrame.fillna()`](kite-sym:pandas.DataFrame.fillna) to fill NaN values in only certain columns {#use-pandas.DataFrame.fillna}
Use the syntax `df[[column_names]]` to select the columns specified by the list `column_names` from the [`DataFrame`](kite-sym:pandas.DataFrame) `df`. Call [`pandas.DataFrame.fillna(value)`](kite-sym:pandas.DataFrame.fillna) with `pandas.DataFrame` as the previous result to replace each `NaN` in `pandas.DataFrame` with `value`.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, 2, 3], "B": [4, np.NaN, 6], "C": [7, 8, np.NaN]})
KITE.set_display_code(True)
print(df)

df[["A", "C"]] = df[["A", "C"]].fillna(0)

print(df)
```
