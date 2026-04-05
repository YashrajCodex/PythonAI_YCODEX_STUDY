# 🐍 Python Notes (Clean + Developer Friendly)

---

## 1. 🖨️ Print & Comments

Print in python is as simple as writing english:

```python
print("Hello world!")
```

- Comments in python use `#`

```python
# this is a comment
```

---

## 2. 📦 Data Types in Python

### 2.1 Types

- `str`, `int`, `float`, `bool`
- `list` (array)
- `dict` (object)
- `set` (unique values)
- `tuple` (locked list)

### 2.2 Dynamic Typing

Data types can be changed:

```python
x = 1
print(x)  # output: 1

x = "the same variable but different data type"
print(x)  # output: the same variable but different data type
```

💡 Python is **dynamically typed** → variable type can change anytime.

---

## 3. ⚙️ Methods

Methods are like functions to work with data types.

Example for strings:

- `upper()`, `lower()`, `title()`

Other methods:

```python
"Hellow World".count('l')   # counts number of time 'l' appears in the string

"Hellow World".replace('o', 'u')   # replaces given string
```

💡 Methods = **data-specific functions**

---

## 4. 🧠 Variables

### 4.1 Creating Variables

```python
text1 = "this is how we can create the variable"
```

---

### 4.2 Naming Rules

✅ Allowed:

```python
_name = "ok"
my_var = 10
age2 = 25
```

❌ Not Allowed:

```python
2age = 16
my-var = "not_ok"
```

---

### 4.3 Swapping Variables (Python Trick ⚡)

```python
a = 5
b = 6
a, b = b, a   # now a = 6, b = 5
```

---

### 4.4 Type Checking

```python
type(variable_name)
```

---

### 4.5 Multiple Assignments

```python
a, b, c = 12, 56, 75
```

---

### 4.6 Reserved Keywords

- `if`, `else`, `for`, `while`, `class`, `def`, `True`, `False`

---

### 4.7 Important Note

- Python variables are **references not boxes**

💡 Think: variable → points to object (not container)

---

## 5. 📋 List (Array in JS)

- Uses `[]`
- Ordered & mutable
- Can store mixed data types

```python
list1 = [1, "hello", True, 3.5]
```

---

### 5.1 Indexing

```python
list1[0]    # 1
list1[-1]   # 3.5
```

---

### 5.2 Slicing

```python
lst = [23, 45, 37, 12, 78]

lst[1:4]   # 45, 37, 12
lst[:3]    # 23, 45, 37
lst[::2]   # 23, 37, 78
```

---

### 5.3 Modify List

```python
lst[0] = 100   # [100, 45, 37, 12, 78]
```

---

### 5.4 Add Elements

```python
list2 = [1, 2]

list2.append(3)        # [1, 2, 3]
list2.insert(1, 99)    # [1, 99, 2, 3]
list2.extend([200, 300])   # [1, 99, 2, 3, 200, 300]
```

---

### 5.5 Remove Elements

```python
list2.remove(2)     # removes first 2 elements of the list
list2.pop()         # removes the last element
list2.pop(2)        # removes element at index 2
del.list[0]         # delete index
list.clear()        # empties the list
```

---

### 5.6 Identity vs Equality ⚠️

```python
a = [1, 2]
b = [1, 2]

print(a == b)   # True (values same)
print(a is b)   # False (different objects)
```

💡 `==` → value compare  
💡 `is` → memory reference compare

---

### 5.7 Looping

```python
for x in list:
    print(x)

# with index
for i in range(len(list)):
    print(list[i])

# best approach
for i, val in enumerate(list):
    print(i, val)
```

---

### 5.8 List Length

```python
len(lst)
```

---

### 5.9 Membership Check

```python
if 2 in lst:
    print("yes")
```

---

### 5.10 Sorting

```python
list.sort()              # mutates original list
sorted.(list)            # returns new list
lst.sort(reverse: True)  # descending order
```

---

### 5.11 Copy

```python
a.copy()
b = a[:]
b = a   # same reference not a copy
```

---

### 5.12 Nested List

```python
list = [[1,2], [3,4]]
lst[0][1]    # Output: 1
```

---

### 5.13 List Comprehension ⚡

```python
lst = [x*x for x in range(5)]
lst = [x for x in range(10) if x % 2 == 0]
```

💡 Pythonic way to write loops

---

### 5.14 Built-in Functions

```python
min(lst)
max(lst)
sum(lst)
```

---

## 6. 📚 Dictionary (Objects in JS)

```python
my_dict = {'key1': 'value1', 'key2': 'value2', 'key3': 'value3'}
```

---

### 6.1 Get Keys

```python
my_dict.keys()
```

---

### 6.2 Get Values

```python
my_dict.values()
```

---

### 6.3 Get Items

```python
my_dict.items()
```

---

### 6.4 Add Items

```python
my_dict['height'] = 1.7
```

---

### 6.5 Update Items

```python
my_dict['height'] = 2.9
```

---

### 6.6 Copy Dictionary

```python
new_dict = my_dict.copy()
```

---

### 6.7 Remove Elements

```python
my_dict.pop(key)
del my_data[key]
my_dict.clear()
```

---

### 6.8 Membership Check

```python
if "name" in my_dict:
    print("exists")
```

---

### 6.9 Length of the dictionary

```python
len(my_dictionary)
```

---

### 6.10 Key must be immutable dictionary

```python
my_dict = {
    1: "num",
    "name": "Yash",
    (1, 2): "tuple",
    [1,2]: "list" #❌ not his
}
```

---

### 6.11 Dictionary comprehension

```python
my_dict = {x: x*x for x in range(5)}
```

---

### 6.12 Merge Dictionaries

```python
d1 = {"a" : 1}
d2 = {"b" : 2}

d = d1 | d2
```

---

## 7. 🔀 If Statements in Python

```python
if <condition>:
    <code>
elif <condition>:
    <code>
else:
    <code>
```

## ⚙ Functions in Python

- Basic function
```python
def greet():            #declare
    print('Hello')

greet()                 #call
```
- With parameters
```python
def printName(name):
    print('This is your name', name)

printName('Yash')
```

- Return values
```python
def printName(a, b):
    return a + b

printName(7, 8)
```
- Multiple return values
```python
def printName(a, b):
    return a + b, a - b

x, y = printName(7, 8)
```

- Default parameters
```python
def printName(name = "Guest"):
    print('This is your name', name)

printName()                 #Output: Guest
printName('Yash')           #Output: Yash
```

- Arbitary arguments
```python
def add_all(*nums):
    return sum(nums)

add_all(7, 8, 8, 7, 30, 60)
```

- Lambda functions
```python
add = lambda a,b: a+b

add(30, 60)
```

---

## Modules in Python

- Module is a file with code like a package in Javascript
- import brings it in.
- 
``` python
import math
print(math.sqrt(16))
```

---


---

## Creating DataFrame in Pandas

- first import pandas and numpy

```python
import pandas as pd
import numpy as np
```

-then create DataFrame using following different ways

#from Python dict (common)
```python
df = pd.DataFrame({
    "name": ["Yash", "Aman"],
    "age": [21,22]
})
```

#from Python lists
```python
data = [
    ["Yash", 21],
    ["Aman", 22]
]
df = pd.DataFrame(data, columns=["name", "age"])
```

#from Python lists of dicts
```python
data = [
    {"name": "Yash", "age": 21}, {"name": "Yash", "age": 22}
]
df = pd.DataFrame(data)
```

#from NumPy array
```python
arr = np.array([[1, 2], [3, 4]])

df = pd.DataFrame(arr, columns= ["A", "B"])
```

#from Random NumPy data
```python

df = pd.DataFrame(np.random.rand(3, 3), columns=["A", "B", "C"])
```
- with Custom Index
  
```python

df = pd.DataFrame([[1, 2], [3, 4]], columns=["A", "B"], index=["row1", "row2"])

```
- to read from CSV/Excel

```python
    df = pd.read_csv("data.csv")
    df = pd.read_csv("data.xlsx")
```
- NumPy is raw numbers
- Pandas is labeled table

---

## Quick inspection
- Attributes
  - df.shape         #to get no of rows and columns
  - df.index           #to get access the index attribute
  - df.columns
  - df.dtypes           #to get datatype of the dataframe
  - 
- Methods
  - pd.set_option('display.max_rows', _no. of rows_)    #to see all or specific number rows.
  - df.head()       #to show first 5 rows of the dataframe
  - df.tail()       #to show last 5 rows of the dataframe
  - df.head(n)       #to show first n rows of the dataframe
  - df.tail(n)       #to show last n rows of the dataframe
  - df.info()       #to get info about the dataframe
  - df.describe()       #to get basic statistics of the dataframe
  - 
---

## Basic functions

- len(df)               #to get total number of rows
- max(df)               #to get highest index of the dataframe
- min(df)               #to get lowest index of the dataframe
- type(df)              #to get the type of dataframe
- round(df, 2)             #to round the values of the dataframe

---

## Single columns from the dataframe

- df.['_column-name_']
- type(df['_column-name_'])
- df.['_column-name_'].index
- df.['_column-name_'].head()

---

## Multiple columns from the dataframe

