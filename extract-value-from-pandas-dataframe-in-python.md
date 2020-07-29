headers:
    use-pd.Series.item: Use `pd.Series.item()`
---
# How to extract a value from a Pandas DataFrame in Python
Extracting a value from a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) gets a specific element from a [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pd.Series.item()`](kite-sym:pandas.Series.item) to extract a value from a [DataFrame](kite-sym:pandas.DataFrame) {#use-pd.Series.item}
Use subsetting to extract a row with a desired element from a [DataFrame](kite-sym:pandas.DataFrame). Call [`row.column.item()`](kite-sym:pandas.Series.item) with `row` as the previouslt extracted row and `column` as the name of the column with the desired value to extract a value.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})
a_row = a_dataframe[a_dataframe["Letters"] == "a"]
value = a_row.Letters.item()

print(value)
```
