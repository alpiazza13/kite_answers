headers:
    iterrows: Use `pandas.DataFrame.iterrows()`
---
# How to iterate over a Pandas DataFrame with a for-loop in Python
Iterating over a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) with a for-loop gives access to each row in the [`DataFrame`](kite-sym:pandas.DataFrame) along with its index.

## Use [`pandas.DataFrame.iterrows()`](kite-sym:pandas.DataFrame.iterrows) to iterate over a DataFrame {#iterrows}
Use the syntax [`for index, row in pandas.DataFrame in df.iterrows()`](kite-sym:pandas.DataFrame.iterrows) to iterate over `pandas.DataFrame`. At each iteration, `row` is the current row in `pandas.DataFrame` and `index` is its index.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"Letters": ["a", "b"], "Numbers": [1, 2]})

#iterate over `df`
for index, row in df.iterrows():
    print(f"Row {index} info:")
    print(row)
```
