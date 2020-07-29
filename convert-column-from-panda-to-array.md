headers:
    use-pandas.loc-or-pandas.iloc-with-pandas.values: Use `pandas.loc()` or `pandas.iloc()` with `pandas.values()`
---
# How to convert a column in a Panda DataFrame to a NumPy array in Python
Converting a column in a DataFrame to a NumPy array generates a list with all the values in the column.

## Use [`pandas.loc.values()`](kite-sym:pandas.core.frame.DataFrame.loc) or [`pandas.iloc()`](kite-sym:pandas.core.frame.DataFrame.iloc) with [`pandas.values()`](kite-sym:pandas.core.series.Series.values) to convert a column into a NumPy array {#use-pandas.loc-or-pandas.iloc-with-pandas.values}

Call `a_dataframe.loc[:, 'column']`, with `column` as the name of the column to be converted, to extract the column to be converted from the DataFrame. Then, call [`values`](kite-sym:pandas.core.series.Series.values) on this result to convert the column into a NumPy array.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Letters': ['a', 'b', 'c'], 'Numbers': [1, 2, 3]})
number_column = a_dataframe.loc[:,'Numbers']
numbers = number_column.values
print(numbers)
```
Or, call `a_dataframe.iloc[:, 'column']`, with `column` as the zero-based index of the column to be converted.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
a_dataframe = pd.DataFrame({'Letters': ['a', 'b', 'c'], 'Numbers': [1, 2, 3]})
number_column = a_dataframe.iloc[:, 1]
numbers = number_column.values
print(numbers)
```
