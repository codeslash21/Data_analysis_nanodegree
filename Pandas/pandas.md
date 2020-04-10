# Pandas:
[Pandas](https://pandas.pydata.org/pandas-docs/stable/reference/index.html#api)

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


