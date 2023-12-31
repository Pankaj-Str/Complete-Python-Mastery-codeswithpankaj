# Python Tuple

## Creating a Tuple

A tuple is created by placing all the items (elements) inside parentheses (), separated by commas. The parentheses are optional, however, it is a good practice to use them.

A tuple can have any number of items and they may be of different types (integer, float, list, string, etc.).

# Different types of tuples
```python
# Empty tuple
my_tuple = ()
print(my_tuple)

# Tuple having integers
my_tuple = (1, 2, 3)
print(my_tuple)

# tuple with mixed datatypes
my_tuple = (1, "Hello", 3.4)
print(my_tuple)

# nested tuple
my_tuple = ("mouse", [8, 4, 6], (1, 2, 3))
print(my_tuple)
```

Output
```python
()
(1, 2, 3)
(1, 'Hello', 3.4)
('mouse', [8, 4, 6], (1, 2, 3))
```

In the above example, we have created different types of tuples and stored different data items inside them.

As mentioned earlier, we can also create tuples without using parentheses:
```python
my_tuple = 1, 2, 3
my_tuple = 1, "Hello", 3.4
```
Create a Python Tuple With one Element

In Python, creating a tuple with one element is a bit tricky. Having one element within parentheses is not enough.

We will need a trailing comma to indicate that it is a tuple,
```python
var1 = ("Hello") # string
var2 = ("Hello",) # tuple
```
We can use the type() function to know which class a variable or a value belongs to.
```python
var1 = ("hello")
print(type(var1))  # <class 'str'>

# Creating a tuple having one element
var2 = ("hello",)
print(type(var2))  # <class 'tuple'>

# Parentheses is optional
var3 = "hello",
print(type(var3))  # <class 'tuple'>
```

Here,
```python
("hello") is a string so type() returns str as class of var1 i.e. <class 'str'>
("hello",) and "hello", both are tuples so type() returns tuple as class of var1 i.e. <class 'tuple'>
```
## Access Python Tuple Elements

Like a list, each element of a tuple is represented by index numbers (0, 1, ...) where the first element is at index 0.

We use the index number to access tuple elements. For example,
## 1. Indexing

We can use the index operator [] to access an item in a tuple, where the index starts from 0.

So, a tuple having 6 elements will have indices from 0 to 5. Trying to access an index outside of the tuple index range( 6,7,... in this example) will raise an IndexError.

The index must be an integer, so we cannot use float or other types. This will result in TypeError.

Likewise, nested tuples are accessed using nested indexing, as shown in the example below.

```python
# Access Python Tuple Elements
# accessing tuple elements using indexing

#       -10   -9   -8   -7   -6   -5   -4   -3   -2   -1
data = ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')
#        0.   1.   2.   3.   4.   5.   6.   7.   8.   9. 

print(data[2]) # w

```
## 2. Negative Indexing
   
Python allows negative indexing for its sequences.

The index of -1 refers to the last item, -2 to the second last item and so on. For example,
```python
# accessing tuple elements using negative indexing
#       -10   -9   -8   -7   -6   -5   -4   -3   -2   -1
data = ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')

print(letters[-1])   # prints 'n' 
print(letters[-3])   # prints '.'
```

## 3. Slicing

We can access a range of items in a tuple by using the slicing operator colon :.
```python
# accessing tuple elements using slicing
data = ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')

# accessing tuple elements using slicing
print(data[2:5]) # output ('w', '.', 'p')
print(data[-9:-3]) # output ('w', 'w', '.', 'p', '4', 'n')
print(data[-5:]) # output ('4', 'n', '.', 'i', 'n')
print(data[:5]) # output ('w', 'w', 'w', '.', 'p')
print(data[:]) # output ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')
```
Output
```python
('w', '.', 'p')
('w', 'w', '.', 'p', '4', 'n')
('4', 'n', '.', 'i', 'n')
('w', 'w', 'w', '.', 'p')
('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')
```

Note: When we slice lists, the start index is inclusive but the end index is exclusive.
Python Tuple Methods

In Python ,methods that add items or remove items are not available with tuple. Only the following two methods are available.

Some examples of Python tuple methods:
```python
# using index function into tuple index()
data = ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')

print(data.index('p')) # output 4
```


```python
# using count function into tuple count()
data = ('w', 'w', 'w', '.', 'p', '4', 'n', '.', 'i', 'n')

print(data.count('w')) # output 3
```
Iterating through a Tuple in Python

We can use the for loop to iterate over the elements of a tuple. For example,
```python
languages = ('Python', 'Swift', 'C++')

# iterating through the tuple
for language in languages:
    print(language)
```

Output
```python
Python
Swift
C++
```
Check if an Item Exists in the Python Tuple

We use the in keyword to check if an item exists in the tuple or not. For example,
```python
languages = ('Python', 'Swift', 'C++')

print('C' in languages)    # False
print('Python' in languages)    # True
```

Here,
```python
'C' is not present in languages, 'C' in languages evaluates to False.
'Python' is present in languages, 'Python' in languages evaluates to True.
```
Advantages of Tuple over List in Python

Since tuples are quite similar to lists, both of them are used in similar situations.

However, there are certain advantages of implementing a tuple over a list:

We generally use tuples for heterogeneous (different) data types and lists for homogeneous (similar) data types.
Since tuples are immutable, iterating through a tuple is faster than with a list. So there is a slight performance boost.
Tuples that contain immutable elements can be used as a key for a dictionary. With lists, this is not possible.
If you have data that doesn't change, implementing it as tuple will guarantee that it remains write-protected.
