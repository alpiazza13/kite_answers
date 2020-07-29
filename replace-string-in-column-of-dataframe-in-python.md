headers:
    use-str.replace: Use `str.replace()`
---
# How to replace a string in a column of a Pandas DataFrame in Python
Replacing a string in a column of a [`DataFrame`](kite-sym:pandas.DataFrame) replaces every instance of a certain string in a column with a different string.

## Use [`str.replace()`](kite-sym:builtins.str.replace) to replace a string in a column of a DataFrame {#use-str.replace}

Call [`str.replace(old, new)`](kite-sym:pandas.DataFrame.iloc) on a column in a DataFrame to replace every instance of the string `old` with the string `new`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a-b", "c-d", "e-f"], "Numbers": [1, 2, 3]})
#replace `- with `_`
a_dataframe["Letters"] = a_dataframe["Letters"].str.replace('-', '_')
print(a_dataframe)
```
