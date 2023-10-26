## List ( )
* In Python, a list is a data structure that can hold an ordered collection of items. These items can be of any data type, including numbers, strings, or even other lists. Lists are defined by enclosing a comma-separated sequence of values within square brackets ([ ]).
* lists are mutable 


```python
help(list)
```

    Help on class list in module builtins:
    
    class list(object)
     |  list(iterable=(), /)
     |  
     |  Built-in mutable sequence.
     |  
     |  If no argument is given, the constructor creates a new empty list.
     |  The argument must be an iterable if specified.
     |  
     |  Methods defined here:
     |  
     |  __add__(self, value, /)
     |      Return self+value.
     |  
     |  __contains__(self, key, /)
     |      Return key in self.
     |  
     |  __delitem__(self, key, /)
     |      Delete self[key].
     |  
     |  __eq__(self, value, /)
     |      Return self==value.
     |  
     |  __ge__(self, value, /)
     |      Return self>=value.
     |  
     |  __getattribute__(self, name, /)
     |      Return getattr(self, name).
     |  
     |  __getitem__(...)
     |      x.__getitem__(y) <==> x[y]
     |  
     |  __gt__(self, value, /)
     |      Return self>value.
     |  
     |  __iadd__(self, value, /)
     |      Implement self+=value.
     |  
     |  __imul__(self, value, /)
     |      Implement self*=value.
     |  
     |  __init__(self, /, *args, **kwargs)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  __iter__(self, /)
     |      Implement iter(self).
     |  
     |  __le__(self, value, /)
     |      Return self<=value.
     |  
     |  __len__(self, /)
     |      Return len(self).
     |  
     |  __lt__(self, value, /)
     |      Return self<value.
     |  
     |  __mul__(self, value, /)
     |      Return self*value.
     |  
     |  __ne__(self, value, /)
     |      Return self!=value.
     |  
     |  __repr__(self, /)
     |      Return repr(self).
     |  
     |  __reversed__(self, /)
     |      Return a reverse iterator over the list.
     |  
     |  __rmul__(self, value, /)
     |      Return value*self.
     |  
     |  __setitem__(self, key, value, /)
     |      Set self[key] to value.
     |  
     |  __sizeof__(self, /)
     |      Return the size of the list in memory, in bytes.
     |  
     |  append(self, object, /)
     |      Append object to the end of the list.
     |  
     |  clear(self, /)
     |      Remove all items from list.
     |  
     |  copy(self, /)
     |      Return a shallow copy of the list.
     |  
     |  count(self, value, /)
     |      Return number of occurrences of value.
     |  
     |  extend(self, iterable, /)
     |      Extend list by appending elements from the iterable.
     |  
     |  index(self, value, start=0, stop=9223372036854775807, /)
     |      Return first index of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  insert(self, index, object, /)
     |      Insert object before index.
     |  
     |  pop(self, index=-1, /)
     |      Remove and return item at index (default last).
     |      
     |      Raises IndexError if list is empty or index is out of range.
     |  
     |  remove(self, value, /)
     |      Remove first occurrence of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  reverse(self, /)
     |      Reverse *IN PLACE*.
     |  
     |  sort(self, /, *, key=None, reverse=False)
     |      Sort the list in ascending order and return None.
     |      
     |      The sort is in-place (i.e. the list itself is modified) and stable (i.e. the
     |      order of two equal elements is maintained).
     |      
     |      If a key function is given, apply it once to each list item and sort them,
     |      ascending or descending, according to their function values.
     |      
     |      The reverse flag can be set to sort in descending order.
     |  
     |  ----------------------------------------------------------------------
     |  Class methods defined here:
     |  
     |  __class_getitem__(...) from builtins.type
     |      See PEP 585
     |  
     |  ----------------------------------------------------------------------
     |  Static methods defined here:
     |  
     |  __new__(*args, **kwargs) from builtins.type
     |      Create and return a new object.  See help(type) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Data and other attributes defined here:
     |  
     |  __hash__ = None
    
    

<b> Syntax :</b> my_list = [item1, item2, item3, ...]



```python
x=[1,2,'three',4.0,5,6]
```


```python
x,type(x),len(x),hex(id(x))

```




    ([1, 2, 'three', 4.0, 5, 6], list, 6, '0x249644a82c0')



## List Indexing :

* ### Positive index : 


```python
x
```




    [1, 2, 'three', 4.0, 5, 6]




```python
x[2]
```




    'three'



### positive slicing:
* In positive indexing,we move from left to right and the start index is '0' and end index is 'n-1',where n is length of the string.


* <b>Syntax : </b>   positive indexing= list [start,end,step size]


```python
x[1:4:1],x[1:4:2]
```




    ([2, 'three', 4.0], [2, 4.0])



### negative indexing :




```python
x
```




    [1, 2, 'three', 4.0, 5, 6]




```python
x[-1]
```




    6



### Nested List :
* list inside the list is called nested list.
* nested list(positive indexing)


```python
x=[1, 2, 'three', 4.0, ['five', 6]]
x
```




    [1, 2, 'three', 4.0, ['five', 6]]




```python
x[4]
```




    ['five', 6]




```python
x[4][1]
```




    6



 ### Negative slicing :
* In negative indexing,we move from <b>right to left</b> and the start index is<b> -1</b> and end index is<b>'-n'</b>,where <b>n</b> is the length of the string

* <b>Syntax : </b>  negative indexing=list[start,end,step size]
* it denotes with negative sign('-')


```python
x
```




    [1, 2, 'three', 4.0, ['five', 6]]




```python
x[-1:-6:-2]
```




    [['five', 6], 'three', 1]



* we cannot use negative stepsizing in a positive index
* syntax must be in same sign


```python
x=[1, 2, 'three', 4.0, ['five', 6]]
```

#### nested list (negative slicing):


```python
x
```




    [1, 2, 'three', 4.0, ['five', 6]]




```python
x[4]
```




    ['five', 6]




```python
x[4][-2]
```




    'five'



### Empty List :
* An empty list in Python is a list that contains no elements. It is represented by a pair of square brackets with nothing in between them. 
* An empty list can be useful as a starting point for collecting and storing data in a list as your program runs. You can add elements to an empty list using various methods like in append() or by directly assigning values to specific indices.


```python
e=[]
```


```python
e
```




    []



### List -class
* In Python, the term "list class" typically refers to the built-in list data type. The list is a fundamental data structure in Python that allows you to store an ordered collection of items. Lists are versatile and can hold elements of different data types, including numbers, strings, and even other lists. They are mutable, which means you can add, remove, and modify elements in a list.
* It can be sequential or non-sequential
* lists are mutable


```python
A=list()
print(A,type(A),len(A),hex(id(A)),sep='\n')
```

    []
    <class 'list'>
    0
    0x24963777200
    


```python
A=['string']  
print(A,type(A),len(A),hex(id(A)),sep='\n')
```

    ['string']
    <class 'list'>
    1
    0x2496371e540
    


```python
A=list('string') ##--->it separates each letter in a given list of a string
A
```




    ['s', 't', 'r', 'i', 'n', 'g']



### sets:
it removes duplicates
### set (list) :
it separates each word in a data type and gives only unique values


```python
l=list({100,1,45,9999})
print(l,type(l),len(l),hex(id(l)),sep='\n')
```

    [1, 100, 45, 9999]
    <class 'list'>
    4
    0x24963754500
    


```python
l=list({100,1,2,3,4,1,100,1000}) ##-->it remove duplicate values ,here 100 and 1 are repeated 2 times but in the out put it gives unique values
print(l,type(l),len(l),sep='\n')
```

    [1, 2, 3, 100, 4, 1000]
    <class 'list'>
    6
    

### Range ( ):

*  In Python, range is a built-in function that is used to generate a sequence of numbers. It is often used in for loops and other situations where you need to iterate over a specific range of values. The range function generates a sequence of integers,and it has the following syntax:
* <b> Syntax : </b>           
* range(stop)
* range(start, stop)
* range(start, stop, step)

where;
* <b>start:</b> The starting value of the range (inclusive). If not specified, it defaults to 0.
* <b>stop: </b>The stopping value of the range (exclusive). The range will generate values up to, but not including, this value.
* <b>step:</b> The step size, which specifies the difference between consecutive values. If not specified, it defaults to 1.



```python
r=range(1,21)
print(r,len(r),type(r),sep='\n')

```

    range(1, 21)
    20
    <class 'range'>
    


```python
s=list(r)
s
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]




```python
s=range(20,0,-1)
list(s)
```




    [20, 19, 18, 17, 16, 15, 14, 13, 12, 11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1]




```python
q=range(0,20,2)
list(q)
```




    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]




```python
x
```




    [1, 2, 'three', 4.0, ['five', 6]]




```python
dir(x)
```




    ['__add__',
     '__class__',
     '__class_getitem__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__getstate__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']



### append :
* In Python, "append" is a method used to add an element to the end of a list. Lists are one of the built-in data types in Python, and they have various methods for manipulating their contents. The append method is specifically used with lists and allows you to add a single element to the end of the list, effectively increasing its length by one.
* It rises an error ,if you add 2 values by using append.It only accepts one value.
* The append method is a common and convenient way to grow a list dynamically by adding new elements to it, one at a time.

<b> Syntax : </b> 
* x=[1,2,3,4]
* x.append(5)
* x.append('string')
* x.append([1,2,3])
       


```python
w=[]
w
```




    []




```python
w.append([1,2,3,4])
w
```




    [[1, 2, 3, 4], [1, 2, 3, 4]]




```python
w.append('string')
w
```




    [[1, 2, 3, 4], [1, 2, 3, 4], 'string', 'string']




```python
#w.append(100,100) ##-->uncomment to see an error
```

### extend ( ):
* In Python, "extend" is a method used to add multiple elements to the end of a list. Like the "append" method, "extend" is used with lists, but it allows you to add all the elements from an iterable (such as another list, tuple, or string) to the end of an existing list. This method effectively increases the length of the list by the number of elements in the iterable you're extending it with.

<b>Syntax :</b> my_list.extend(iterable)

where;
* iterable is the iterable containing the elements you want to add to the end of the list.



```python
c=[1,2,3,7,8,9]
c.extend([0,4,5,6])
c
```




    [1, 2, 3, 7, 8, 9, 0, 4, 5, 6]




```python
c=[1,2,3,7,8,9]
d=[0,5,4,6]
c.extend(d)
c
```




    [1, 2, 3, 7, 8, 9, 0, 5, 4, 6]



###  Insert :

* In Python, "insert" is a method used to add an element at a specific position within a list. Lists are one of the built-in data types in Python, and they have various methods for manipulating their contents. The insert method is used with lists and allows you to specify both the index (position) where you want to insert an element and the element you want to insert.

<b> Syntax : </b> 
* x=[21,22]
* x.insert(index, item)

where;
* Where x is the list you want to insert an element into, index is the position where you want to insert the element, and item is the element you want to insert.



```python
b=[2,4,5,6]
b.insert(1,3)
b
```




    [2, 3, 4, 5, 6]



### pop and remove
* These methods are used for removing the values

 ### Remove :
 * In Python, "remove" is a method used with lists to remove the first occurrence of a specified element from the list. Lists are one of the built-in data types in Python, and they have various methods for manipulating their contents. The remove method is used when you want to eliminate a specific element from the list based on its value, not its index.
 
 <b> Syntax : </b> my_list.remove(item)
 
 where;
 * item is the element you want to remove.



```python
y=list('malayalam')
y
```




    ['m', 'a', 'l', 'a', 'y', 'a', 'l', 'a', 'm']




```python
y.remove('a') ##--->it removes first occurence of a letter you given
y
```




    ['m', 'l', 'y', 'a', 'l', 'a', 'm']



### pop :
* In Python, "pop" is a method used with lists to remove and return an element from a specific position in the list. Lists are one of the built-in data types in Python, and they have various methods for manipulating their contents. The pop method is used when you want to remove an element based on its index and, by default, it removes the element from the end of the list (the last element).

<b>Syntax :</b> my_list.pop(index)

where;
* Where my_list is the list you want to remove an element from, and index is the position of the element you want to remove.



```python
v=[1,2,3,4,5]
u=v.pop(3)
u
```




    4




```python
u,v
```




    (4, [1, 2, 3, 5])




```python
v
```




    [1, 2, 3, 5]




```python
v.pop() ##-->by default it removes last element of the list
```




    5




```python

```
