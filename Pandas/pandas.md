# Pandas:
[Pandas](https://pandas.pydata.org/pandas-docs/stable/reference/index.html#api) is built on the top of Numpy.

## Pandas Seris:
This is Pandas 1-D data structure like Numpy Array but with extra functionalities. The values are ordered.

### Similarities with NumPy:
* Accessing elements: `s[0], s[1:3]`
* Looping: `for x in s`
* Convenient Functions: `s.mean(), s.max()`
* Vector operations.
* Implemented in C like Numpy.

```
import pandas as pd
l = pd.Seris([1,2,3,4],
             index = ['a', 'b', 'c', 'd'])
print(l) # a 1
           b 2
           c 3
           d 4
           
l[0] # 1
l.loc['b'] # 2 loc is used to look up for values by their index
```
```
import pandas as pd
l = pd.Seris([1,2,3,4])
print(l) # 0 1
           1 2
           2 3
           3 4
           
l[0] # 1
l.iloc[1] # 2 iloc is used to look up for values by their position
```
## Vectorized operations:
```
l1 = pd.Seris([1,2,3,4],
             index = ['a', 'b', 'c', 'd'])
l2 = pd.Seris([10,20,30,40],
             index = ['a', 'b', 'c', 'd'])
l1 + l2 #  a 11
           b 22
           c 33
           d 44
```
```
l1 = pd.Seris([1,2,3,4],
             index = ['a', 'b', 'c', 'd'])
l2 = pd.Seris([10,20,30,40],
             index = ['d', 'c', 'b', 'a'])
l1 + l2 #  a 41
           b 32
           c 23
           d 14
```
```
l1 = pd.Seris([1,2,3,4],
             index = ['a', 'b', 'c', 'd'])
l2 = pd.Seris([10,20,30,40],
             index = ['a', 'b', 'e', 'f'])
l1 + l2 #  a 11
           b 22
           c NaN
           d NaN
           e NaN
           f NaN
```
```
l1 = pd.Seris([1,2,3,4],
             index = ['a', 'b', 'c', 'd'])
l2 = pd.Seris([10,20],
             index = ['a', 'b'])
s = l1 + l2
s #  a 11
     b 22
     c NaN
     d NaN
     
s.dropna() # a 11
             b 22
           
l1.add(l2, fill_value=0) # a 11
                            b 22
                            c 3
                            d 4
```
## apply() method:
This is same as map for list. It works on pandas Series. If there is such needed function thst is not built-in then that function can be applied to the `Series` by apply() method. e.g. `s.apply(fn(3)), wher fn() is the applied function & s is the pd.Seris()`

## Plotting:
* If the variable `data` is a NumPy array or a Pandas Series, just like if it is a list, the code
```
import matplotlib.pyplot as plt
plt.hist(data)
```
will create a histogram of the data.
* Pandas also has built-in plotting that uses matplotlib behind the scenes, so if `data` is a Series, you can create a histogram using `data.hist()`.
*  Sometimes the Pandas wrapper can be more convenient. For example, you can make a line plot of a series using `data.plot()`. The index of the Series will be used for the x-axis and the values for the y-axis.


## DataFrame:
This is a 2D data structure of Pandas. This is more flexible to use over Numpy 2D Array. Every column of DataFrame can has different datatypes. If we apply `mean()` function over a DataFrame object then it will calculate mean for only those columns which has `int` or `float` type data. Index can be provided for the dataframe.
```
import pandas as pd
df = pd.DataFrame({
    'int':[1,2,3,4],
    'float':[1.0,2.0,3.0,4.0],
    'char':['a','b','c','d']
},index=[1,2,3,4])

    int   float   char
1    1     1.0     a
2    2     2.0     b
3    3     3.0     c
4    4     4.0     d
```
* accessing element by index
```
df.loc[1] # int 1
            float 1.0
            char a
            
df.loc[2,'float'] # 2.0
```
* access element by column name
```
df['float'] # 1 1.0
              2 2.0
              3 3.0
              4 4.0
```
* accessing element by position
```
df.iloc[3] # int 4
            float 4.0
            char d
            
df.iloc[0,2] # a ,this is at row=0 and col=2

```
* get only values i.e. 2D Array (of Numpy)
```
df.values # array([[1, 1.0, 'a'],
                   [2, 2.0, 'b'],
                   [3, 3.0, 'c'],
                   [4, 4.0, 'd']])
```
* get index of max in a row
```
df.loc[1].argmax() # to get index of max of row 1(by index)
```
* get mean
```
df.mean() # this gives mean for every column possible
df[:, 'float'].mean() # to get mean for 'float' column
df.values.mean() # this gives mean for all data set
```

## Plotting with DataFrame:
DtaFrame is a simple wrapper around matplotlib functions.
`% matplotlib inline` - this is an important line to include when plotting in Jupyter Notebook.
* `df.hist()` to creat `Histogram` for every column.
* `df.hist(figsize=(8,8));` to increase size of diagrams and `;` is for removing unwanted output.
* `df['col_name'].hist();` To create histogram for a particular column.
* `df['col_name'].plot(kind='hist');` to create histogram for a particular column.
* `df['col_name'].value_counts()` To count occurrence of each unique value.
* `df['col_name'].value_counts().plot('bar');` To plot bar diagram for a particular column.
* `df['col_name'].value_counts().plot('pie', figsize=(8,8));` To plot pie diagram for a particular column.
* `df.plot(x='col_name_1', y='col_name_2', kind='scatter');` To get scatter plot with two columns to get correlation.

## NOTE:
* To fill the `NaN` there is `fillna()` function to apply with the value to place instead of null.
```
mean = df['col_name'].mean()
df['col_name'] = df['col_name']fillna(mean)
```
* To find the duplicates in the dataset we have required function -
```
df.duplicated() # this returns true/false for every row and return true for the row where duplicate occures excluding the first occurence

sum(df.duplicated()) # by this one can detect the number of duplicacy in the dataset(as True=1 and False=0).

df.drop_duplicates(inplace=True) # this remove the rows where True comes as duplicacy.
```
* `df['datetime'] = pd.to_datetime(df['datetime'])` to chage datatype to datetime.
* By default, Pandas' std() function computes the standard deviation using Bessel's correction. Calling std(ddof=0) ensures that Bessel's correction will not be used. [Bessel's correction](https://en.wikipedia.org/wiki/Bessel%27s_correction)
* By default, numpy calculates a population standard deviation, with `ddof = 0`. On the other hand, pandas calculates a sample standard deviation, with `ddof = 1`.

## Panel:
`Panel` is Pnadas 3D data structure similar to DataFrame or Series. [Documentation](https://pandas.pydata.org/pandas-docs/stable/getting_started/dsintro.html)
