headers:
    use-pandas.DataFrame.replace: Use `pandas.DataFrame.replace()`
---
# How to replace each empty string in a pandas DataFrame with NaN in Python
Replacing each empty string in a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) with `NaN` converts any strings with only whitespace to `NaN`.

## Use [`pandas.DataFrame.replace()`](kite-sym:pandas.DataFrame.replace) replace each empty string with NaN {#use-pandas.DataFrame.replace}
Call [`pandas.DataFrame.replace(to_replace, value, regex=True)`](kite-sym:pandas.DataFrame.replace) with `to_replace` as `r"^\s*$"` and `value` as [`numpy.NaN`](kite-sym:numpy.NaN) to replace and empty strings or strings containing only spaces with `NaN`.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
df = pd.DataFrame({"A": ["    ", "b", "c"], "B": ["d", "e", ""]})

df = df.replace(r'^\s*$', np.NaN, regex=True)

print(df)
```
