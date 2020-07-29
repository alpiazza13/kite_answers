
headers:
    use-datetime.date: Use `datetime.date()`
---
## How to extract the dates from a column of datetime objects in a Pandas DataFrame in Python
Extracting the dates from a column of [datetime](kite-sym:datetime) objects in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) removes the time info from each element in the column.

## Use [`datetime.date()`](kite-sym:datetime.date) extract the dates from a column  {#use-datetime.date}
Use [`column.dt.date`](kite-sym:datetime.date) with `column` as a column of datetime objects to extract only the dates from `column`.

```python
KITE.start_prelude()
import pandas as pd
import datetime as dt
KITE.stop_prelude()
dates = [dt.datetime(2000, 1, 1, 5, 0, 0), dt.datetime(2010, 1, 5, 7, 0, 0), dt.datetime(2015, 2, 5, 5, 0, 0)]
a_dataframe = pd.DataFrame({"ID": ["1", "2", "3"], "Date": dates})
a_dataframe["Date"] = a_dataframe["Date"].dt.date

print(a_dataframe)
```
