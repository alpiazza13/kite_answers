headers:
    use-pandas.apply: Use `pandas.apply()`
---
# How to create a new column based on values from other columns in a Pandas DataFrame in Python
The values in a new column in a [`DataFrame`](kite-sym:pandas.DataFrame) can be based on those in existing columns.

## Use [`pandas.apply()`](kite-sym:pandas.core.frame.DataFrame.apply)  {#use-pandas.apply}

Call `dataframe[new_column] = dataframe.apply(function, axis = 1)` to apply `function` to each row in `dataframe` and add the resulting column to `dataframe` with the title `new_column`. In the code below, `function` is an [anonymous function](https://www.w3schools.com/python/python_lambda.asp).
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Length': [1, 2, 3], 'Width': [1, 2, 3]})
a_dataframe['Area'] = a_dataframe.apply(lambda row: row.Length * row.Width, axis=1)
print(a_dataframe)
```
