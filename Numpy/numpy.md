# Numpy(Numerical Python):
[NumPy](https://docs.scipy.org/doc/numpy/)

## Array:
Its `1-D` data structure of numpy. Its almost similar to python `List`. Example:
```
L=[a,b,c,d]
```
Below is the similarities -
### Similarities:
* Each element can be accessed by index. E.g. `L[0]=a`.
* Access a range of elements. E.g. `L[1:3]=[b,c]`.
* Use loops, e.g. `for x in L:`.
### Differences:
* Each element should be of same type unlike python List. That means each element should be int or float or char and so on.
* There are some special methods like - `mean()`, `std()` and can be multi dimensional.

### Operations:
#### Vectorized operation:
* Addition: `[1,2,3] + [4,5,6] = [5,7,9]`
* Subtraction: `[1,2,3] - 1 = [0,1,2]`
* Scalar multi: `[1,2,3] * 3 = [3,6,9]`
* Other operations:
  * Math operations(+, -, /, *, **).
  * Logical operations(&, |, ~).
  * Comparison operations(>, >=, <, <=, ==, !=).
  
## Index Array:
Suppose there are two arrays of same length and the second list contains booleans,
```
a = [1,2,3,4,5]
b = [F,F,T,T,T]
a[b] = [3,4,5]
a[a>2] = [3,4,5]
```
`b` is called `index array` and it tells you which elements of the first array to keep.

## + vs += :
```
import numpy as np
a = np.array([1,2,3])
b = a
a += np.array([1,1,1])
print(a) # [2,3,4]
print(b) # [2,3,4]  
```
as `a` and `b` both pointing to the same array.
```
import numpy as np
a = np.array([1,2,3])
b = a
a = a + np.array([1,1,1])
print(a) # [2,3,4]
print(b) # [1,2,3] 
```
here initially `a` and `b` both pointing to the same array, but later `a` is refered to the new array that is `a + [1,1,1] means [2,3,4]`
`+=` is `in place` operator means this store the new value to the same place where the old value was stored and `+` is `not in place` operator which store new value to the new place.
This is also same for `python list()`.
## Slicing Array:
```
import numpy as np
a = np.array([1,2,3])
b = a[:2]
b[0]=10
print(a) # [10, 2, 3]
print(b) # [10, 2]
```
