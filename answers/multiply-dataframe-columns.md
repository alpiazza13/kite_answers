headers:
    use-indexing: Use DataFrame indexing
---
# How to multiply two columns of a pandas DataFrame in Python
Multilpying two columns of a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) adds a new column to the [`DataFrame`](kite-sym:pandas.DataFrame) with each value as the product of the corresponding values in the multiplied columns.

## Use [`DataFrame`](kite-sym:pandas.DataFrame) indexing to multiply two columns of a DataFrame {#use-indexing}
Use the syntax `df[column1] * df[column2]` to multiply the columns named `column1` and `column2` in the [`DataFrame`](kite-sym:pandas.DataFrame) `df`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
KITE.set_display_code(False)
df = pd.DataFrame({"A": [1, 2, 3], "B": [4, 5, 6]})
KITE.set_display_code(True)
print(df)

df["C"] = df["A"] * df["B"]

print(df)
```
