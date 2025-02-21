# Reference guide: Lists

You’ve been learning that lists are important data structures in Python. A list is a data structure that helps store and manipulate an ordered collection of items. These items can be of any data type such as integers, floats, strings, and even other lists. Because they are so versatile, data professionals and all Python programmers use lists every day, so it’s important to be familiar with how they work. This reading is a reference guide for lists designed to help you as you learn Python.

## **Create a list**

There are two main ways to create lists in Python:

* Square brackets: `[]`  
* The list function:  `list()`

When instantiating a list using brackets, separate each element with a comma. For example, the following code creates a list of strings:  
list\_a \= \['olive', 'palm', 'coconut'\]

You can also create a list of integers:  
list\_b \= \[8, 6, 7, 5, 3, 0, 8\]

Or a list of mixed data types:  
list\_c \= \['Abidjan', 14.2, \[1, 2, None\], 'Zagreb'\]

To create an empty list, use empty brackets or the `list()` function:  
empty\_list\_1 \= \[\]  
empty\_list\_2 \= list()

The `list()` function can also convert iterable data types to lists:  
my\_string \= 'Wilson'  
my\_list \= list(my\_string)  
print(my\_list)

## **Indexing and slicing**

Just as with strings, you can access elements in a list using indexing and slicing. The first element of a list has index zero, the second element has index one, and so on. Use square brackets to index:  
phrase \= \['Astra', 'inclinant', 'sed', 'non', 'obligant'\]  
print(phrase\[1\])

You can also use negative indices to access items from the end of a list:  
phrase \= \['Astra', 'inclinant', 'sed', 'non', 'obligant'\]  
print(phrase\[\-1\])

Use slicing to extract a sublist. To slice, use square brackets containing a range of indices separated by a colon:  
phrase \= \['Astra', 'inclinant', 'sed', 'non', 'obligant'\]  
print(phrase\[1:4\])

Notice that this code returned a sublist containing the elements at indices one, two, and three of `phrase`. The ending index of the slice is not included.

Omitting the starting index in a slice implies an index of zero, and omitting the ending index implies an index of `len(my_list)`:  
phrase \= \['Astra', 'inclinant', 'sed', 'non', 'obligant'\]  
print(phrase\[:3\])  
print(phrase\[3:\])

## **List mutability**

Lists are mutable, which means that you can change their contents after they are created. You can change an individual item in a list by specifying its index and assigning a new value to it. For example:  
my\_list \= \['Macduff', 'Malcolm', 'Duncan', 'Banquo'\]  
my\_list\[2\] \= 'Macbeth'  
print(my\_list)

You can even change a slice of a list using the same logic. The slice can be of any length. The elements in the new list will be inserted in place of the indicated slice:   
my\_list \= \['Macduff', 'Malcolm', 'Macbeth', 'Banquo'\]  
my\_list\[1:3\] \= \[1, 2, 3, 4\]  
print(my\_list)

## **List operations**

Lists can be combined using the addition operator (`+`):  
num\_list \= \[1, 2, 3\]  
char\_list \= \['a', 'b', 'c'\]  
num\_list \+ char\_list

They can also be multiplied using the multiplication operator (\*):  
list\_a \= \['a', 'b', 'c'\]  
list\_a \* 2

But they cannot be subtracted or divided. 

You can check whether a value is contained in a list by using the `in` operator:  
num\_list \= \[2, 4, 6\]  
print(5 in num\_list)  
print(5 not in num\_list)

## **List methods**

Lists are a core Python class. As you’ve learned, classes package data together with tools to work with it. Methods are functions that belong to a class. Lists have a number of built-in methods that are very useful. These include:

### 

### `append()`

Add an element to the end of a list:  
my\_list \= \[0, 1, 1, 2, 3\]  
variable \= 5  
my\_list.append(variable)  
print(my\_list)

### `insert()` 

Insert an element at a given position:  
my\_list \= \['a', 'b', 'd'\]  
my\_list.insert(2, 'c')  
print(my\_list)

### `remove()` 

Remove the first occurrence of an item:  
my\_list \= \['a', 'b', 'd', 'a'\]  
my\_list.remove('a')  
print(my\_list)

### `pop()` 

Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list:  
my\_list \= \['a', 'b', 'c'\]  
my\_list.pop()  
print(my\_list)

### `clear()` 

Remove all items:  
my\_list \= \['a', 'b', 'c'\]  
my\_list.clear()  
print(my\_list)

### 

### `index()` 

Return the index of the first occurrence of an item in the list:  
my\_list \= \['a', 'b', 'c', 'a'\]  
my\_list.index('a')

### `count()` 

Return the number of times an item occurs in the list:  
my\_list \= \['a', 'b', 'c', 'a'\]  
my\_list.count('a')

### `sort()` 

char\_list \= \['b', 'c', 'a'\]  
num\_list \= \[2, 3, 1\]  
char\_list.sort()  
num\_list.sort(reverse=True)  
print(char\_list)  
print(num\_list)

## **Additional resources**

* For more information about lists, refer to [An Informal Introduction to Python: Lists](https://docs.python.org/3/tutorial/introduction.html#lists).  
* For more list methods, refer to [Data Structures: More on Lists](https://docs.python.org/3/tutorial/datastructures.html).

