headers:
    use-pandas.DataFrame.isnull: Use `pandas.DataFrame.isnull()`
---
# How to find rows with NaN values in a pandas DataFrame in Python
Finding rows with NaN values in a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) selects each row with at least one `NaN` from the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pandas.DataFrame.isnull()`](kite-sym:pandas.DataFrame.isnull) to find rows with NaN values {#use-pandas.DataFrame.isnull}
Call [`pandas.DataFrame.isnull()`](kite-sym:pandas.DataFrame.isnull) to get a boolean [`DataFrame`](kite-sym:pandas.DataFrame) indicating whether each value in `pandas.DataFrame` is `NaN`. Call [`pandas.DataFrame.any(axis=1)`](kite-sym:pandas.DataFrame.any) to get a boolean [`Series`](kite-sym:pandas.Series) indicating whether each row in the previous result `pandas.DataFrame` contains at least one `True`. Subset the original [`DataFrame`](kite-sym:pandas.DataFrame) using this result.

```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [np.NaN, 2, 3], "B": [4, 5, np.NaN]})
KITE.set_display_code(True)
print(df)

is_NaN = df.isnull()
row_has_NaN = is_NaN.any(axis=1)
rows_with_NaN = df[row_has_NaN]

print(rows_with_NaN)
```
