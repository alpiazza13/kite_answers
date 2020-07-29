headers:
    index: Use `pandas.DataFrame.index()`
---
# How to set the index title in a Pandas DataFrame in Python
Setting the index title in a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) adds a label to the index of the [`DataFrame`](kite-sym:pandas.DataFrame).

## Use [`pandas.DataFrame.index`](kite-sym:pandas.DataFrame.index) set the index title {#index}
Access the index of a DataFrame with [`pandas.DataFrame.index`](kite-sym:pandas.DataFrame.index). Assign a title to the `name` attribute of the index.

```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
df = pd.DataFrame({"Letters": ["a", "b", "c"], "Numbers": [1, 2, 3]})

index = df.index
index.name = "Index Title"

print(df)
```
