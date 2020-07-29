headers:
    use-pandas.DataFrame.loc: Use `pandas.DataFrame.loc`
---
# How to print a row of a Pandas DataFrame in Python
Printing a row of a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) displays a specified row from a [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pandas.DataFrame.loc`](kite-sym:pandas.DataFrame.loc) to print a row {#use-pandas.DataFrame.loc}

Use [`pandas.DataFrame.loc`](kite-sym:pandas.DataFrame.loc) to access a row in `pandas.DataFrame` by its index. Use the indexing syntax `[[index]]` to display a row.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})

# get second row
second_row = df.loc[[1]]
print(second_row)
```
