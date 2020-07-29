headers:
    use-pandas.DataFrame.fillna: Use `pandas.DataFrame.fillna()`
---
# How to replace NaN values with empty strings in a pandas DataFrame in Python
Replacing NaN values with empty strings in a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) fills any missing values in the [`DataFrame`](kite-sym:pandas.DataFrame) with `""`.

## Use [`pandas.DataFrame.fillna()`](kite-sym:pandas.DataFrame.fillna) to replace NaN values with empty strings {#use-pandas.DataFrame.fillna}
Call [`pandas.DataFrame.fillna(value)`](kite-sym:pandas.DataFrame.fillna) with `value` as `""` to replace each `NaN` in `pandas.DataFrame` with `value`.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, "b", "c"], "B": ["d", "e", np.NaN]})
KITE.set_display_code(True)
print(df)

df = df.fillna("")

print(df)
```
