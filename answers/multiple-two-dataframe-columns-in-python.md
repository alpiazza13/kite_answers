headers:
    use-index: Use `DataFrame` indexing
---
# How to multiply two pandas DataFrame columns in Python
Multiplying two [`pandas.DataFrame`](kite-sym:pandas.DataFrame) columns results in a new column containing the product of the two other columns. For example, multiplying `[1, 2, 3]` and `[4, 5, 6]` results in `[4, 10, 18]`.

## Use DataFrame indexing to multiply two columns {#use-indexing}
Use the syntax `df[col1] * df[col2]` with `df` as a [`DataFrame`](kite-sym:pandas.DataFrame) and `col1` and `col2` as column names from `df`. Assign the result to a new column in the [`DataFrame`](kite-sym:pandas.DataFrame).
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"a": [1, 2, 3], "b": [4, 5, 6]})

#multiply columns `"a"` and `"b"`
df["a*b"] = df["a"] * df["b"]

print(df)
```
