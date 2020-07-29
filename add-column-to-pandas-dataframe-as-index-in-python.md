headers:
    use-pd.DataFrame.set_index: Use `pd.DataFrame.set_index()`
---
# How to add a column to a Pandas Dataframe as the index in Python
Adding a column to a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) as the index replaces a [Dataframe's](kite-sym:pandas.DataFrame) default zero-based index with a new column.

## Use [`pd.DataFrame.set_index()`](kite-sym:pandas.DataFrame.set_index) to set a new column as the index {#use-pd.DataFrame.set_index}
Add the desired index column to a [DataFrame](kite-sym:pandas.DataFrame). Then use [`pd.DataFrame.set_index(keys)`](kite-sym:pandas.DataFrame.set_index) with `keys` as the column name to make `keys` the index of `pd.DataFrame`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Continent": ["Asia", "Europe", "Africa"], "Language": ["Mandarin", "French", "English"]})
countries = ["China", "Belgium", "South Africa"]
a_dataframe["Countries"] = countries
#make countries the index
a_dataframe = a_dataframe.set_index("Countries")
belgium = a_dataframe.loc["Belgium", :]

print(belgium)
```
