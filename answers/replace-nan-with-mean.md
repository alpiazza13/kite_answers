headers:
    use-pandas.DataFrame.fillna: Use `pandas.DataFrame.fillna()`
---
# How to replace each NaN value in a pandas DataFrame with the mean of its column in Python
Replacing each NaN value in a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) with the mean of its column fills each missing value in the [`DataFrame`](kite-sym:pandas.DataFrame) with the average of its column.

## Use [`pandas.DataFrame.fillna()`](kite-sym:pandas.DataFrame.fillna) to replace each NaN value with the mean of its column {#use-pandas.DataFrame.fillna}
Call [`pandas.DataFrame.mean()`](kite-sym:pandas.DataFrame.mean) to get a [`Series`](kite-sym:pandas.Series) with the mean of each column of `pandas.DataFrame`. Call [`pandas.DataFrame.fillna(value)`](kite-sym:pandas.DataFrame.fillna) with `value` as the previous result to replace each `NaN` in `pandas.DataFrame` with `value`.

```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, 2, 3], "B": [4, 5, np.NaN]})
KITE.set_display_code(True)
print(df)

column_means = df.mean()
df = df.fillna(column_means)

print(df)
```
