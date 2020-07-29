headers:
​	use-group-by-and-head: Use `pandas.DataFrame.groupby()` and `pandas.DataFrame.head()`
---

# How to get the top n entries of a pandas DataFrame column in Python

Getting the top `n` entries of a [`pandas.DataFrame`](kite-sym:pandas.DataFrame) column results in a [pandas.Series](kite-sym:pandas.DataFrame) containing only the first `n` entries in the specified column.

## Use [`pandas.Series.head()`](kite-sym:pandas.Series.head) to get the top n entires of a DataFrame column {#use-group-by-and-head}
Call [`pandas.Series.head(n)`](kite-sym:pandas.Series.head) with `pandas.Series` as `pandas.DataFrame[name]` to get the first `n` entries in the column named `named` from `pandas.DataFrame`.


```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
KITE.set_display_code(False)
letters = ["a","b","c","d","e"]
numbers = [1, 2, 3, 4, 5]
df = pd.DataFrame(list(zip(letters, numbers)), columns = ["Letters", "Numbers"])
KITE.set_display_code(True)
print(df)

top_two_letters = df["Letters"].head(2)

print(top_2_letters)
```
