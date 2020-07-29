headers:
    use-a-for-loop: Use a for-loop
---
# How to iterate over columns of a Pandas DataFrame in Python
Iterating over columns of a [`DataFrame`](kite-sym:pandas.DataFrame) gives access to each individual column of a DataFrame.

## Use a for-loop to iterate over columns of a DataFrame  {#use-a-for-loop}
Use the loop `for column in pd.DataFrame` to iterate over each `column` in `pd.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
for column in a_dataframe:
    this_column = a_dataframe[column]
    print(this_column)
```
