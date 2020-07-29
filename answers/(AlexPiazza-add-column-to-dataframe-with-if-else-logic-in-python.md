headers:
    select: Use `numpy.select()`
---
# How to add a column to a Pandas DataFrame using if-else logic in Python
Adding a column to a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) using if-else logic adds a column with elements determined by a list of conditions.

## Use [`numpy.select()`](kite-sym:numpy.select) to add a column using if-else logic {#select}
Assign a new column to the result of [`numpy.select(condlist, choicelist, default=value)`](kite-sym:numpy.select) with `condlist` as a list of conditions and `choicelist` as a list of choices. If the i-th element in `condlist` is `True`, then the i-th element of the new column will be the i-th element of `choicelist`. If multiple conditions are satisfied, the first one in `condlist` is used. If all conditions are `False`, `value` is used.
```python
KITE.start_prelude()
import pandas as pd
import numpy as np
KITE.stop_prelude()
df = pd.DataFrame({"A": [0, 0, 1, 1], "B": [0, 1, 0, 1]})

condition_one = (df["A"] == 0) & (df["B"] == 0)
condition_two = (df["A"] == 1) | (df["B"] == 1)
conditions = [condition_one, condition_two]
choices = ["False", "True"]
#add "A or B" column
df["A or B"] = np.select(conditions, choices, default="")

print(df)
```
