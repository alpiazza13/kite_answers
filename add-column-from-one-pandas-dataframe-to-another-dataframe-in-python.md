headers:
    use-pandas.DataFrame.join: Use `pandas.DataFrame.join()`
---
# How to add a column from a Pandas DataFrame to another DataFrame in Python
Adding a column from a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) to another [`DataFrame`](kite-sym:pandas.DataFrame) updates a [`DataFrame`](kite-sym:pandas.DataFrame) with a new column from another [`DataFrame`](kite-sym:pandas.DataFrame).


## Use [`pandas.DataFrame.join()`](kite-sym:pandas.DataFrame.join) to add a column from a DataFrame to another DataFranme {#use-pandas.DataFrame.join}
Use [`pandas.DataFrame.join(other)`](kite-sym:pandas.DataFrame.join) with `other` as a column from another [`DataFrame`](kite-sym:pandas.DataFrame) to add `other` to `pandas.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df1 = pd.DataFrame({"Letters": ["a", "b", "c"]})
df2 = pd.DataFrame({"Letters": ["d", "e", "f"], "Numbers": [1, 2, 3]})

numbers = df2["Numbers"]
# add `numbers` to `df1`
df1 = df1.join(numbers)

print(df1)
```
