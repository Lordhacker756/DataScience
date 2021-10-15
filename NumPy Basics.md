# Basic Functions


```python
import numpy as np
array1 = np.array([[1,2,3,4,5],[6,7,8,9,10]])
print(array1)
```

    [[ 1  2  3  4  5]
     [ 6  7  8  9 10]]
    


```python
array1.shape
```




    (2, 5)




```python
array1.dtype
```




    dtype('int32')



#Arrays in numpy


```python
np.ones((5,5))
```




    array([[1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.]])




```python
array1**array1
```




    array([[         1,          4,         27,        256,       3125],
           [     46656,     823543,   16777216,  387420489, 1410065408]],
          dtype=int32)



# Slicing In NumPy


```python
arr = np.array([1,2,3,4,5,6])
```

Slicing the elements from 1st to 4th we have, ⚠️This is a view of it not a copy,any change you do to this sliced part will reflect in the orignal array


```python
sliced = arr[1:4]
print(sliced)
```

    [2 3 4]
    


```python
sliced[2] = 8
print(sliced)
print(arr)
```

    [2 3 8]
    [1 2 3 8 5 6]
    

This is what im talking about as sliced array was its part hence, changing the sliced part also changed the orignal array, to counter this problem we use , arr[1,4].copy(), this creates a copy and whatever change we do doesnt effect the main data


```python
array1
```




    array([[ 1,  2,  3,  4,  5],
           [ 6,  7,  8,  9, 10]])


