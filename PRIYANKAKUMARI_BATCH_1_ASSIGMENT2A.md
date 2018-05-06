# Assignment 2A
## Python101

## Priyanka Kumari | Batch 1
### Data Type

eip = 3
print(type(eip))  # Prints "<class 'bool'>"
print(eip)       # Prints "3"
print(eip+ 1)   # Addition; prints "4"
print(eip - 1)   # Subtraction; prints "2"
print(eip * 2)   # Multiplication; prints "6"
print(eip ** 2)  # Exponentiation; prints "9"
eip += 1
print(eip)  # Prints "4"
eip *= 2
print(eip)  # Prints "8"
mlblr = 2.5
print(type(mlblr)) # Prints "<class 'float'>"
print(mlblr, mlblr + 1, mlblr * 2, mlblr ** 2) # Prints "2.5 3.5 5.0 6.25"


### Numbers

eip = True
mlblr = False
print(type(eip)) # Prints "<class 'bool'>"
print(eip and mlblr) # Logical AND; prints "False"
print(eip or mlblr)  # Logical OR; prints "True"
print(not eip)   # Logical NOT; prints "False"
print(t != mlblr)

### Strings in Python

eip_in = 'hello'    # String literals can use single quotes
eip_out = "world"    # or double quotes; it does not matter.
print(eip_in)       # Prints "hello"
print(len(eip_in))  # String length; prints "5"
eip = eip_in + ' ' + eip_out  # String concatenation
print(eip)  # prints "hello world"
mlblr = '%s %s %d' % (eip_in, world, 12)  # sprintf style string formatting
print(mlblr)  # prints "hello world 12"

### Useful methods

mlblr = "hello"
print(mlblr.capitalize())  # Capitalize a string; prints "Hello"
print(mlblr.upper())       # Convert a string to uppercase; prints "HELLO"
print(mlblr.rjust(7))      # Right-justify a string, padding with
spaces; prints "  hello"
print(mlblr.center(7))     # Center a string, padding with spaces;
prints " hello "
print(mlblr.replace('l', '(ell)'))  # Replace all instances of one
substring with another; # prints "he(ell)(ell)o"
print('  world '.strip())  # Strip leading and trailing whitespace;
prints "world"

### Python Containers - List

eip_list = [3, 1, 2]    # Create a list
print(eip_list, eip_list[2])  # Prints "[3, 1, 2] 2"
print(eip_list[-1])     # Negative indices count from the end of the
list; prints "2"
eip_list[2] = 'foo'     # Lists can contain elements of different types
print(eip_list)         # Prints "[3, 1, 'foo']"
eip_list.append('bar')  # Add a new element to the end of the list
print(eip_list)         # Prints "[3, 1, 'foo', 'bar']"
mlblr = eip_list.pop()      # Remove and return the last element of the list
print(mlblr, eip_list)      # Prints "bar [3, 1, 'foo']"

### Slicing

mlblr_in = list(range(5))     # range is a built-in function that
creates a list of integers
print(mlblr_in)               # Prints "[0, 1, 2, 3, 4]"
print(mlblr_in[2:4])          # Get a slice from index 2 to 4
(exclusive); prints "[2, 3]"
print(mlblr_in[2:])           # Get a slice from index 2 to the end;
prints "[2, 3, 4]"
print(mlblr_in[:2])           # Get a slice from the start to index 2
(exclusive); prints "[0, 1]"
print(mlblr_in[:])            # Get a slice of the whole list; prints
"[0, 1, 2, 3, 4]"
print(mlblr_in[:-1])          # Slice indices can be negative; prints
"[0, 1, 2, 3]"
mlblr_in[2:4] = [8, 9]        # Assign a new sublist to a slice
print(mlblr_in)               # Prints "[0, 1, 8, 9, 4]"

### Loops

eip = ['cat', 'dog', 'monkey']
for animal in animals:
    print(eip) # Prints "cat", "dog", "monkey", each on its own line.

### Enumerate

mlblr = ['cat', 'dog', 'monkey']
for idx, animal in enumerate(animals):
    print('#%d: %s' % (idx + 1, mlblr)) # Prints "#1: cat", "#2: dog",
"#3: monkey", each on its own line

### Dictionaries

eip = {'cat': 'cute', 'dog': 'furry'}  # Create a new dictionary with some data
print(eip['cat'])     # Get an entry from a dictionary; prints "cute"
print('cat' in eip)     # Check if a dictionary has a given key; prints "True"
eip['fish'] = 'wet'     # Set an entry in a dictionary
print(eip['fish'])      # Prints "wet"
print(eip['monkey'])  # KeyError: 'monkey' not a key of d
print(eip.get('monkey', 'N/A'))  # Get an element with a default; prints "N/A"
print(eip.get('fish', 'N/A'))    # Get an element with a default; prints "wet"
del eip['fish']         # Remove an element from a dictionary
print(eip.get('fish', 'N/A')) # "fish" is no longer a key; prints
"N/A"# It is easy to iterate over the keys in a dictionary

eip = {'person': 2, 'cat': 4, 'spider': 8}
for animal in eip:
    legs = eip[animal]
    print('A %s has %d legs' % (animal, legs))# Prints "A person has 2
legs", "A cat has 4 legs", "A spider has 8 legs"

### Dictionary Comprehension

/# If you want access to keys and their corresponding values, use the
items method:

eip = {'person': 2, 'cat': 4, 'spider': 8}
for animal, legs in d.items():
    print('A %s has %d legs' % (animal, legs)) # Prints "A person has
2 legs", "A cat has 4 legs", "A spider has 8 legs"

### Dictionary comprehension

eip = [0, 1, 2, 3, 4]
mlblr = {eip_in: eip_in** 2 for eip_in in eip if eip_in % 2 == 0}
print(mlblr)  # Prints "{0: 0, 2: 4, 4: 16}"

### Sets

eip = {'cat', 'dog'}
print('cat' in eip)   # Check if an element is in a set; prints "True"
print('fish' in eip)  # prints "False"
eip.add('fish')       # Add an element to a set
print('fish' in eip)  # Prints "True"
print(len(eip))       # Number of elements in a set; prints "3"
animals.add('cat')        # Adding an element that is already in the
set does nothing
print(len(eip))       # Prints "3"
eip.remove('cat')     # Remove an element from a set
print(len(eip))       # Prints "2"

### Tuples

eip = {(x, x + 1): eip_in for eip_in in range(10)}  # Create a
dictionary with tuple keys
mlblr = (5, 6)        # Create a tuple
print(type(mlblr))    # Prints "<class 'tuple'>"
print(eip[mlblr])       # Prints "5"
print(eip[(1, 2)])  # Prints "1"

### Functions

def sign(eip):
    if eip > 0:
        return 'positive'
    elif eip < 0:
        return 'negative'
    else:
        return 'zero'

for eip in [-1, 0, 1]:
    print(sign(eip)) # Prints "negative", "zero", "positive"

### Function Arguments

def eip_in(name, eip_out=False):
    if eip_out:
        print('HELLO, %s!' % name.upper())
    else:
        print('Hello, %s' % name)

eip_in('Bob') # Prints "Hello, Bob"
eip_in('Fred', eip_out=True)  # Prints "HELLO, FRED!"

### NumPy

import numpy as eip_in

eip = eip_in.array([1, 2, 3])   # Create a rank 1 array
print(type(eip))            # Prints "<class 'numpy.ndarray'>"
print(eip.shape)            # Prints "(3,)"
print(eip[0], eip[1], eip[2])   # Prints "1 2 3"
eip[0] = 5                  # Change an element of the array
print(eip)                  # Prints "[5, 2, 3]"

mlblr = eip_in.array([[1,2,3],[4,5,6]])    # Create a rank 2 array
print(mlblr.shape)                     # Prints "(2, 3)"
print(mlblr[0, 0], mlblr[0, 1], mlblr[1, 0])   # Prints "1 2 4"

### Some NumPy Functions

import numpy as eip

eip_in = eip.zeros((2,2))   # Create an array of all zeros
print(eip_in)              # Prints "[[ 0.  0.]
                           #[ 0.  0.]]"

eip_out = eip.ones((1,2))    # Create an array of all ones
print(eip_out)              # Prints "[[ 1.  1.]]"

mlblr_in = eip.full((2,2), 7)  # Create a constant array
print(mlblr_in)               # Prints "[[ 7.  7.]  #[ 7.  7.]]"

mlblr_out = eip.random.random((2,2))  # Create an array filled with
random values
print(mlblr_out)                     # Might print "[[ 0.91940167  0.08143941]
                                     # [ 0.68744134  0.87236687]]"


Mixing integer indexing with slice indexing

### import numpy as eip

/# Create the following rank 2 array with shape (3, 4)
/# [[ 1  2  3  4]
/#  [ 5  6  7  8]
/#  [ 9 10 11 12]]
mlblr = eip.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])

/# Two ways of accessing the data in the middle row of the array.
eip_in = mlblr[1, :]    # Rank 1 view of the second row of a
eip_out = mlblr[1:2, :]  # Rank 2 view of the second row of a
print(eip_in, eip_in.shape)  # Prints "[5 6 7 8] (4,)"
print(eip_out, eip_out.shape)  # Prints "[[5 6 7 8]] (1, 4)"

### Datatypes

import numpy as eip

mlblr = eip.array([1, 2])   # Let numpy choose the datatype
print(mlblr.dtype)         # Prints "int64"

x = eip.array([1.0, 2.0])   # Let numpy choose the datatype
print(mlblr.dtype)             # Prints "float64"

mlblr = eip.array([1, 2], dtype=eip.int64)   # Force a particular datatype
print(mlblr.dtype)

### Array Math

import numpy as eip

eip_in = eip.array([[1,2],[3,4]], dtype=np.float64)
eip_out = eip.array([[5,6],[7,8]], dtype=np.float64)

print(eip.add(eip_in, eip_out)) # or print(eip_in + eip_out) # [[ 6.0
8.0] #  [10.0 12.0]]

print(eip.subtract(eip_in, eip_out)) or print(eip_in - eip_out) #
[[-4.0 -4.0] #  [-4.0 -4.0]]

print(eip.multiply(eip_in, eip_out)) or print(eip_in * eip_out) # [[
5.0 12.0] #  [21.0 32.0]]

print(eip.divide(eip_in, eip_out)) or print(eip_in / eip_out) # [[ 0.2
0.33333333] #  [ 0.42857143  0.5       ]]

print(eip.sqrt(eip_in)) # [[ 1. 1.41421356] #  [ 1.73205081  2.]]

### Dot function

import numpy as eip

eip_in = eip.array([[1,2],[3,4]])
eip_out = eip.array([[5,6],[7,8]])

mlblr_in = eip.array([9,10])
mlblr_out = eip.array([11, 12])

/# Inner product of vectors; both produce 219
print(mlblr_in.dot(mlblr_out))
print(eip.dot(mlblr_in, mlblr_out))

/# Matrix / vector product; both produce the rank 1 array [29 67]
print(eip_in.dot(mlblr_in))
print(eip.dot(eip_in, mlblr_in))

/# Matrix / matrix product; both produce the rank 2 array
/# [[19 22] #  [43 50]]
print(x.dot(eip_out))
print(eip.dot(eip_in, eip_out))

### Sum along an axis

import numpy as eip

mlblr = eip.array([[1,2],[3,4]])

print(eip.sum(mlblr))  # Compute sum of all elements; prints "10"
print(eip.sum(mlblr, axis=0))  # Compute sum of each column; prints "[4 6]"
print(eip.sum(mlblr, axis=1))  # Compute sum of each row; prints "[3 7]"


### MathPlotLib - Plotting Graphs

import numpy as eip
import matplotlib.pyplot as plt

/# Compute the x and y coordinates for points on a sine curve
eip_in = eip.arange(0, 3 * eip.pi, 0.1)
eip_out = eip.sin(x)

/# Plot the points using matplotlib
plt.plot(eip_in, eip_out)
plt.show()  # You must call plt.show() to make graphics appear.

### Images

import numpy as eip
from scipy.misc import imread, imresize
import matplotlib.pyplot as mlblr

/# Uncomment the line below if you're on a notebook
/# %matplotlib inline
eip_in = imread('assets/cat.jpg')
img_tinted = eip_in * [1, 0.95, 0.9]

/# Show the original image
mlblr.subplot(1, 2, 1)
mlblr.imshow(img)

/# Show the tinted image
mlblr.subplot(1, 2, 2)

/# A slight gotcha with imshow is that it might give strange results
/# if presented with data that is not uint8. To work around this, we
/# explicitly cast the image to uint8 before displaying it.
mlblr.imshow(np.uint8(img_tinted))
mlblr.show()

