headers:
    use-in: Use `in`
---
# How to check if a column exists in a Pandas DataFrame in Python
A Pandas DataFrame has one or more columns, each of which can have a name to identify it.

## Use `in` to check if a column is in a DataFrame {#use-in}

Check if the column is in the DataFrame with `column_name in dataframe`, with `column_name` as the name of the column to be checked and `dataframe` as the name of the DataFrame object.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Letters': ['a', 'b'], 'Numbers': [1, 2]})
letters_in_dataframe = 'Letters' in a_dataframe
print(letters_in_dataframe)
```
