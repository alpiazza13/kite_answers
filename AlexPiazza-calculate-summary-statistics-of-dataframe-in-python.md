headers:
    use-pd.describe: Use `pd.describe()`
---
# How to calculate summary statistics of a Pandas DataFrame in Python
Calculating summary statistics of a [DataFrame](kite-sym:pandas.core.frame.DataFrame) gets certain statistics for each numeric column in a DataFrame.
## Use [`pd.describe()`](kite-sym:pandas.core.frame.DataFrame.describe) to calculate summary statistics of a DataFrame {#use-pd.describe}
Call [`dataframe.describe()`](kite-sym:pandas.core.frame.DataFrame.describe) to get statistics from `dataframe`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1, 2, 3, 4], "Name": ["Alex", "Jake", "Alex", "Jake"], "Age": [10, 5, 20, 10]})
statistics = a_dataframe.describe()
print(statistics)
```
