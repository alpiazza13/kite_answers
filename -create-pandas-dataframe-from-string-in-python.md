headers:
    use-pandas.read_csv: Use `pandas.read_csv()`
---
# How to create a Pandas DataFrame from a string in Python
Creating a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) from a string results in a [`DataFrame`](kite-sym:pandas.DataFrame) defined by a string of data.


## Use [`pandas.read_csv()`](kite-sym:pandas.read_csv) to create a DataFrame from a string {#use-pandas.read_csv}
Use [`io.StringIO(string)`](kite-sym:io.StringIO) with `string` as a string of data to get a `StringIO` object. To create a [`DataFrame`](kite-sym:pandas.DataFrame), use [`pandas.read_csv(filepath_or_buffer, sep=delimiter)`](kite-sym:pandas.read_csv) with `filepath_or_buffer` as the previous result and `sep` assigned to the character that separates each row entry in `string`.
```python
KITE.start_prelude()
import pandas as pd
import io
KITE.stop_prelude()
data_string = """Letters, Numbers
                 a, 1
                 b, 2
                 c, 3"""

data = io.StringIO(data_string)
#create DataFrame from `data`
df = pd.read_csv(data, sep=",")

print(df)
```
