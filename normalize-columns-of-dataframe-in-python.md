
headers:
    use-pd.DataFrame.std-and-pd.DataFrame.mean: Use `pd.DataFrame.mean()` and `pd.DataFrame.std()`
---
# How to normalize the elements of a Pandas DataFrame in Python
Normalizing the columns of a Pandas [`DataFrame`](kite-sym:pandas.DataFrame) converts each element in a [`DataFrame`](kite-sym:pandas.DataFrame) to its [z-score](https://www.statisticshowto.datasciencecentral.com/probability-and-statistics/z-score/).

## Use [`pd.DataFrame.mean()`](kite-sym:pandas.DataFrame.mean) and [`pd.DataFrame.std()`](kite-sym:pandas.DataFrame.std) to normalize a DataFrame {#use-pd.DataFrame.std-and-pd.DataFrame.mean}
Calculate the distance from the mean of each element in a [`DataFrame`](kite-sym:pandas.DataFrame) with [`pd.DataFrame - pd.DataFrame.mean()`](kite-sym:pandas.DataFrame.mean). Calculate the standard deviation of a [`DataFrame`](kite-sym:pandas.DataFrame) with [`pd.DataFrame.std()`](kite-sym:pandas.DataFrame.std). Then, for each element, divide its distance from the mean by the standard deviation to calculate its z-score.
```python
KITE.start_prelude()
import pandas as pd
KITE.stop_prelude()
a_dataframe = pd.DataFrame({"Data1": [10, 20, 30], "Data2": [10, 20, 30]})
distance_from_mean = a_dataframe - a_dataframe.mean()
standard_deviation = a_dataframe.std()
normalized_dataframe = distance_from_mean / standard_deviation
print(normalized_dataframe)
