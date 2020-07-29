headers:
    use-pd.DataFrame.apply: Use `pd.DataFrame.apply()`
---
# How to apply a function to two columns in a Pandas DataFrame in Python
Applying a function to two single column in a [`DataFrame`](kite-sym:pandas.DataFrame) changes the elements in those columns using a given function.

## Use [`pd.DataFrame.apply()`](kite-sym:pandas.DataFrame.apply) to apply a function to two columns in a DataFrame  {#use-pd.DataFrame.apply}
Use `pd.DataFrame[[column_1, column_2]]` to extract two columns from `pd.DataFrame`. Call [`columns.apply(func, axis=1)`] to change the elements in `columns`, the DataFrame obtained from the above extraction, using `func`, a function which takes one input.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1, 2, 3], "Age": [10, 20, 30], "Weight": [80, 100, 120]})
def add_one(x):
    return x + 1
a_dataframe[["Age", "Weight"]] = a_dataframe[["Age", "Weight"]].apply(add_one, axis=1)
print(a_dataframe)
```
To apply a function to two columns in a DataFrame and create a new column combining the values of those two columns, assign `func(column_1, column_2)` to a new column in a DataFrame, with `func` as a function which takes two inputs.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"ID": [1, 2, 3], "Age": [10, 20, 30], "Weight": [80, 100, 120]})
def add(x,y):
    return x + y
a_dataframe["Age + Weight"] = add(a_dataframe["Age"], a_dataframe["Weight"])
print(a_dataframe)
```
