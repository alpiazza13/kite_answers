headers:
    use-pd.DataFrame.apply: Use `pd.DataFrame.apply()`
---
# How to apply a function to a single column in a Pandas DataFrame in Python
Applying a function to a single column in a [`DataFrame`](kite-sym:pandas.DataFrame) changes the elements in a column using a given function.

## Use [`pd.DataFrame.apply()`](kite-sym:pandas.DataFrame.apply) to apply a function to a single column in a DataFrame  {#use-pd.DataFrame.apply}
Call [`column.apply(func)`](kite-sym:pandas.DataFrame.apply), with `column` as a column in a DataFrame to change the elements in `column` using `func`, a function which takes one input.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
def add_one(x):
    return x + 1
# add one to all elements in "Numbers"
a_dataframe["Numbers"] = a_dataframe["Numbers"].apply(add_one)
print(a_dataframe)
```
