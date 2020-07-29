headers:
    concatenate: Use `pandas.concat()`
---
# How to merge two Pandas Series into a DataFrame in Python
Merging two Pandas [`Series`](kite-sym:pandas.Series) into a [`DataFrame`](kite-sym:pandas.DataFrame) in Python creates a [`DataFrame`](kite-sym:pandas.DataFrame) with columns as the two [`Series`](kite-sym:pandas.Series).

## Use [`pandas.concat(objs, axis=1)`](kite-sym:pandas.concat) to merge two Series {#concatenate}
Use [`pandas.concat(objs, axis=1)`](kite-sym:pandas.concat) with `objs` as a sequence of two [`Series`](kite-sym:pandas.Series) to create a [`DataFrame`](kite-sym:pandas.DataFrame).

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_series = pd.Series(["a", "b", "c"], name="Letters")
another_series = pd.Series([1, 2, 3], name="Numbers")

#merge `a_series` and `another_series`
df = pd.concat([a_series, another_series], axis=1)

print(df)
```
