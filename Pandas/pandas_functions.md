# Pandas Functions:
```
import pandas as pd
s # its a Pandas Series object
df # its a DataFrame object
```
* `df.add(s, axis='index'/'columns')` To add dataframe to seris. If `axis=index` then each element of the series will be added to subsequent rows of the dataframe otherwise will be added to the columns.
* `df + s` is similar to `df.add(s, axis='columns')`.
* `df.apply()` To apply not built-in functions, but it will apply function to the entire column at a time and every column of the dataframe. This is useful for get how much an element is away from the sd for a particular column.
* `df.applymap()` to apply not built-in functions. This apply function to every element of the dataframe.
* `df.div(s, axis='index'/'columns')` To divide the dataframe index/column wise.
* `df.duplicated()` To get which row has duplicate value
* `sum(df.duplicated())` To get total number of duplicated row
* `df['col_name'].plot(kind='hist');` To create histogram for a particular column.
* `df.plot(x='col_name_1', y='col_name_2', kind='scatter');` To get scatter plot with two columns to get correlation.
* `df['col_name'].value_counts()` To count occurrence of each unique value.
* `df['col_name'].value_counts().plot('bar');` To plot bar diagram for a particular column.
* `df['col_name'].value_counts().plot('pie', figsize=(8,8));` To plot pie diagram for a particular column.
* `diff()` To get differences between two subsequent rows. 
* `drop_duplicates(inplcae=True)` To remove the duplicated rows.
* `df.groupby['col_name'].groups` To group particular column based on the unique values.
* `df.groupby['col_name'].sum()` To group and get sum of corresponding values for each of unique values.
* `df.groupby['col_name'].sum()['value_col'].mean()` To get mean of the values og the groups.
There is a argument called is_index and set `is_index=False` for not to get col_name as index.

* `df.hist()` To create histograms for all possible columns.
* `df.info()` To get brief information about every column.
* `df.mean(axis='columns'/'index')` To calculate mean by index/columns.
* `df.merge(df1, on = [lists_of_col_names], how='inner/left/right')` To merge two dataframes.
* `df.shift(period=(int))` To shift by given periods. [shift()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.shift.html)
* `df.std(axis='columns'/'index')` To calculate std by index or columns.
*  `s.sort_values()` To sort pandas series.

