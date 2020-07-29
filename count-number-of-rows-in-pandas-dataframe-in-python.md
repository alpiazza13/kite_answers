headers:
    index: Use `pandas.DataFrame.index()`
---
# How to count the number of rows in a Pandas DataFrame in Python
Counting the number of rows in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) determines how many rows exist in the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pandas.DataFrame.index`](kite-sym:pandas.DataFrame.index) to count the number of rows {#index}
Access the index of a DataFrame with [`pandas.DataFrame.index`](kite-sym:pandas.DataFrame.index). Call [`len(obj)`](kite-sym:builtins.len) with `obj` as the index to find the number of rows.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})

index = df.index
#find length of index
number_of_rows = len(index)

print(number_of_rows)

```
