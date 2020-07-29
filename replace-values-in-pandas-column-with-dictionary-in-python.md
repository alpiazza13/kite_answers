headers:
    use-pd.DataFrame.replace: Use `pd.DataFrame.replace()`
---
# How to replace a Pandas DatFrame column using a dictionary in Python
Replacing a column in a [`DataFrame`](kite-sym:pd.DataFrame) changes the values in a column to those in a dictionary.

## Use [`pd.DataFrame.replace()`](kite-sym:pandas.DataFrame.replace) to replace a column using a dictionary  {#use-pd.DataFrame.replace}
Call [`pd.DataFrame.replace(to_replace, value)`](kite-sym:pandas.DataFrame.replace) with `to_replace` as the name of a column to replace with `value`, a dictionary mapping elements in `to_replace` to new elements.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
a_dict = {1: 4, 2: 5, 3: 6}
#replace "Numbers" using a_dict
new_dataframe = a_dataframe.replace("Numbers", a_dict)
print(new_dataframe)
```
