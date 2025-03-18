**Reference guide: Arrays**

As you’ve learned, NumPy is a powerful library capable of performing advanced numerical computing. One of its main features is its ability to work with vectors, arrays, and matrices. The NumPy library also has many useful mathematical functions. Data professionals use NumPy for many different tasks. One of its primary advantages is its speed. An operation applied to a vector executes much faster than the same operation applied to a list. Performance increases become apparent when working with large volumes of data. This reading is a reference guide for working with NumPy arrays. 

## **Create an array**

Remember that to use NumPy, you must first import it. Standard practice is to alias it as `np`. 

### [`np.array()`](https://numpy.org/doc/stable/reference/generated/numpy.array.html)

Creates an `ndarray` (n-dimensional array). There is no limit to how many dimensions a NumPy array can have, but arrays with many dimensions can be more difficult to work with.

#### 1-D array:

import numpy as np  
array\_1d \= np.array(\[1, 2, 3\])  
array\_1d

Notice that a one-dimensional array is similar to a list.

#### 2-D array:

array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
array\_2d

Notice that a two-dimensional array is similar to a table.

#### 3-D array:

array\_3d \= np.array(\[\[\[1, 2\], \[3, 4\]\], \[\[5, 6\], \[7, 8\]\]\])  
array\_3d

Notice that a three-dimensional array is similar to two tables.

### [`np.zeros()`](https://numpy.org/doc/stable/reference/generated/numpy.zeros.html)

* Creates an array of a designated shape that is pre-filled with zeros:  
  np.zeros((3, 2))

### [`np.ones()`](https://numpy.org/doc/stable/reference/generated/numpy.ones.html)

* Creates an array of a designated shape that is pre-filled with ones:  
  np.ones((2, 2))

### [`np.full()`](https://numpy.org/doc/stable/reference/generated/numpy.full.html)

* Creates an array of a designated shape that is pre-filled with a specified value:  
  np.full((5, 3), 8)


These functions are useful for various situations, including:

* To initialize an array of a specific size and shape and then subsequently fill it with values derived from a calculation  
* To allocate memory for later use  
* To perform matrix operations

## **Array methods**

NumPy arrays have many methods that allow you to manipulate and operate on them. For a full list of these, refer to the [NumPy array documentation](https://numpy.org/doc/stable/reference/arrays.ndarray.html). Some of the most commonly used methods include:

### [`ndarray.flatten()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.flatten.html)

* Returns a copy of the array collapsed into one dimension  
  array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  array\_2d.flatten()

### [`ndarray.reshape()`](https://numpy.org/doc/stable/reference/generated/numpy.reshape.html#numpy.reshape)

* Gives a new shape to an array without changing its data  
  array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  array\_2d.reshape(3, 2)  
    
  Note that a value of \-1 in the designated new shape indicates for NumPy to infer the value based on other given values. This is for user convenience.  
  array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  array\_2d.reshape(3, \-1)


### [`ndarray.tolist()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.tolist.html)

* Converts an array to a list object. Multidimensional arrays are converted to nested lists.   
  array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  array\_2d.tolist()


### Mathematical functions

NumPy arrays also have many methods that are mathematical functions, such as:

* [`ndarray.max()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.max.html): returns the maximum value in the array or along a specified axis  
* [`ndarray.mean()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.mean.html): returns the mean of all the values in the array or along a specified axis  
* [`ndarray.min()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.min.html): returns the minimum value in the array or along a specified axis  
* [`ndarray.std()`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.std.html): returns the standard deviation of all the values in the array or along a specified axis  
  a \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  print(a.max())  
  print(a.mean())  
  print(a.min())  
  print(a.std())


## **Array attributes**

NumPy arrays have several attributes that allow you to access information about the array. Some of the most commonly used attributes include:

* [`ndarray.shape`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.shape.html): returns a tuple of the array’s dimensions  
* [`ndarray.dtype`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.dtype.html): returns the data type of the array’s contents  
* [`ndarray.size`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.size.html): returns the total number of elements in the array  
* [`ndarray.T`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.T.html): returns the array transposed (rows become columns, columns become rows)  
  array\_2d \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
  print(array\_2d.shape)  
  print(array\_2d.dtype)  
  print(array\_2d.size)  
  print(array\_2d.T)


## **Indexing and slicing**

You can access individual elements of a NumPy array using indexing and slicing. Indexing in NumPy is similar to indexing in Python lists, except you can use multiple indices to access elements in multidimensional arrays.  
a \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
print(a\[1\])  
print(a\[0, 1\])  
print(a\[1, 2\])

You can also use slicing to access subarrays of a NumPy array:  
a \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
print(a)  
a\[:, 1:\]

## **Array operations**

NumPy arrays support many operations, including mathematical functions and arithmetic operations. These include array addition and multiplication, which performs element-wise arithmetic on arrays:  
a \= np.array(\[(1, 2, 3), (4, 5, 6)\])  
b \= np.array(\[\[1, 2, 3\], \[1, 2, 3\]\])  
print(a \+ b)  
print(a \* b)

There are also nearly 100 other useful [mathematical functions](https://numpy.org/doc/stable/reference/routines.math.html#mathematical-functions) that can be applied to individual and/or multiple arrays.

## **Mutability**

NumPy arrays are mutable, but with certain limitations. For instance, you can change an existing element of an array:  
a \= np.array(\[(1, 2), (3, 4)\])  
a\[1\]\[1\] \= 100  
a

However, you cannot lengthen or shorten the array:  
a \= np.array(\[1, 2, 3\])  
a\[3\] \= 100  
a

### How NumPy arrays store data in memory

NumPy arrays work by allocating a contiguous block of memory at the time of instantiation. Other structures in Python don’t do this. Their data is scattered across the system’s memory. This is what makes NumPy arrays so fast. All the data is stored together at a particular address in the system’s memory. However, this is also what prevents you from being able to lengthen or shorten the array. The abutting memory is occupied by other information. There’s no room for more data at that memory address. However, you can replace existing elements of the array with new elements.   
![A diagram of system memory. A NumPy array sits directly in between other data structures. There’s no room to add values.][image1]  
The only way to lengthen an array is to copy the existing array to a new memory address along with the new data. 

[image1]: <data:image/png;base64,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Sy6xpwAAVUCAA5AZnfe2aNEizn8DgGoiwAEAADiGAAcAAOAYAhwAAIBjCHAAAACOIcABAAA4hgAHAADgGAIcAACAYwhwAAAAjiHAAQAAOIYABwAA4BgCHAAAgGMIcAAAAI4hwAEAADiGAAcAAOAYAhwAAIBjCHAAAACOIcABAAA4hgAHAADgGAIcAACAYwhwAAAAjiHAAQAAOIYABwAA4BgCHAAAgGMIcAAAAI4hwAGrqGXLlpnHH3/cHsYq4scff7SHADiEAAesojp16mTGjh1bNPbLL7+YBx54oKg++uijomXghnfffbdoPT7yyCNF8y+++KLZa6+9zPfff180DsANBDhgFXTfffeZAw880Pzwww9F49qY53I506NHj0LdddddRcvoMZdeemksECTlu+++MzfeeKM58cQTzWWXXWY++eQTe5Fq+/jjj4PnX7hwofnpp5/s6URpT+eMGTPMp59+ak+ttA8//NDMnz+/qO6///6iZa699trCOuzQoYNp06ZN0bx07drV/P73v2dvHOAgAhywinnnnXdM27Zt7eFAGOBKUdjp2bNnsMyZZ55pT1fbv//97yBwaO/grrvuagYNGmTWWGMNe7FqeeKJJ0yLFi3MuHHjglCz9dZbm59//tleLDH77rtv8PP673//a0+ttHvuucc0btzYjBo1qlDHH3+8vViBwl15Ae6VV14Jxo844gh7CkAtV/qdGoCXFCj69etnDwcqC3C33367ufzyy4OQlXSA0+Hb3/3ud0Gwih7W23nnnSNLVZ/2IIZ7q5577rmg33vvvddaKhmLFy82derUSTzAXX/99aZ///72cEmlApxcddVVpkGDBubVV1+1pwDUYqXfqQFP6BCcNqCnnnqq6dy5s9lhhx1Mu3btgsNQoaZNm5qDDjooONQ0YsQIU79+/eCwVFXo8XvssYeZNGlScGhq8ODBRYfNunXrZvbee+/gv6NHjzY77rijadiwYXB+kkydOtUMGDDA7LTTTsHGuaysLHg9of322y/YCOt7TJw40XTp0sV8/vnnwZwOgXXs2LEoVF1xxRXBnqboIUIFsHr16pkvv/yyMBZVWYAL6XUmHeBKOeecc+yhxDz99NNBv0uXLrWnqm3ChAlm2223NQ899FDiAe6UU04JDn0+++yz5rHHHgvCb0UqCnBy9NFHm4EDB9rDAGqxyt+pAceF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>