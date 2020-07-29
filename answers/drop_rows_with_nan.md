headers:
    use-pandas.DataFrame.dropna: Use `pandas.DataFrame.dropna()`
---
# How to drop rows with NaN values from a pandas DataFrame in Python
Dropping rows with NaN values from a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) removes any rows with one or missing value from the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pandas.DataFrame.dropna()`](kite-sym:pandas.DataFrame.dropna) to drop rows with NaN values {#use-pandas.DataFrame.dropna}
Call [`pandas.DataFrame.dropna()`](kite-sym:pandas.DataFrame.dropna) to drop all rows with `NaN`'s from `pandas.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, 2, 3], "B": [4, 5, np.NaN]})
KITE.set_display_code(True)
print(df)

df = df.dropna()

print(df)
```
