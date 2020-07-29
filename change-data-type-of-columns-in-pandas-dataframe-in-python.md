headers:
    use-pandas.astype: Use `pandas.astype()`
---
# How to change the data type of columns in a Pandas DataFrame in Python
Changing the data type of a column in a [`DataFrame`](kite-sym:pandas.DataFrame) converts each object in a column to a specified type.

## Use [`pandas.astype()`](kite-sym:pandas.core.frame.DataFrame.astype)  {#use-pandas.astype} to change the data type of selct columns

Call [`dataframe.astype(column_type_dictionary)`](kite-sym:pandas.core.frame.DataFrame.astype) to change the types of columns in `dataframe` based on a dictionary with keys as column names and values as data types.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Column 1': [1, 2, 3], 'Column 2': ["1", "2", "3"]})
a_dataframe = a_dataframe.astype({"Column 1": float, "Column 2": int})
type_of_column_1 = a_dataframe['Column 1'].dtype
type_of_column_2 = a_dataframe['Column 2'].dtype
print(type_of_column_1, type_of_column_2)
```
