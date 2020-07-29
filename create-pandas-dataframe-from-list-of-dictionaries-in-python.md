headers:
    use-DataFrame-initializiation: Use DataFrame initialization
---
# How to create a Pandas DataFrame from a list of dictionaries in Python
Creating a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) from a list of dictionaries results in a [`DataFrame`](kite-sym:pandas.DataFrame) with entries defined by a list of dictionaries.

## Use [`DataFrame`](kite-sym:pandas.DataFrame) initialization to create a DataFrame from a list of dictionaries {#use-DataFrame-initializiation}
Use the syntax [`pd.DataFrame(data)`](kite-sym:pandas.DataFrame) with `data` as a list of dictionaries to create a [`DataFrame`](kite-sym:pandas.DataFrame) from `data`.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
data = [{"Letters" : "a", "Numbers": 1},
        {"Letters": "b", "Numbers": 2},
        {"Letters": "c", "Numbers": 3}]

# create a DataFrame from `data`
df = pd.DataFrame(data)
print(df)
```
