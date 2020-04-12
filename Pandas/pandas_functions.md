# Pandas Functions:
```
import pandas as pd
df # its a DataFrame object
```
* `df.duplicated()` To get which row has duplicate value
* `sum(df.duplicated())` To get total number of duplicated row
* `df.drop_duplicates(inplcae=True)` To remove the duplicated rows.
* `df.hist()` To create histograms for all possible columns.
* `df.info()` To get brief information about every column.
* `df['col_name'].plot(kind='hist');` To create histogram for a particular column.
* `df.plot(x='col_name_1', y='col_name_2', kind='scatter');` To get scatter plot with two columns to get correlation.
* `df['col_name'].value_counts()` To count occurrence of each unique value.
* `df['col_name'].value_counts().plot('bar');` To plot bar diagram for a particular column.
* `df['col_name'].value_counts().plot('pie', figsize=(8,8));` To plot pie diagram for a particular column.
