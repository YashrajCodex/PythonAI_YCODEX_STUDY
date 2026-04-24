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
  - df.columns          #to get list of all the columns in a dataframe
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

- df[['col1', 'col2']]
- df.loc[:, ["col1", "col2"]]             # means rows all and 2 columns
- df.loc[:, [0, 2]]                       # selecting by index. this selects 1 and 3 columns
- df.loc[:, 0:2]                          # selecting column in range. this selects 0 and 1 columns {2 excluded}
- df.filter(like='sales')                 # selecting column starting with something case sensetive
- df.loc[:, df.columns != "age"]          # selecting column conditionally. This returns all columns except "age".
- df.filter(regex="^a")                   # selecting column using regex. This returns columns starting with 'a'.
- new_df = df[["name", "age"]]            # select and assign columns at the same time

---

## Add a new column in the dataframe

- df["new_column"] = 100                  #adds a column with same value for all rows
- df["total"] = df['price'] * df['quantity']                  #adds a derived column buy multiplying 2 column
- df['status'] = df['score'].apply(lambda x: "Pass" if x>50 else "Fail")           #adds a conditional column buy checking the value of other column
- df['status'] = np.where(df['score'] > 50, "Pass", "Fail")           #same result as above but using a powerfull module: NumPy
- df['name_upper'] = df["name"].str.upper()           #works because columns have method. This creates a new column with all uppercase letters of name column
- df.insert(1, "new_column", df["price"] * 2)           #insert at specific position. This adds at index 1.

# Math Operations

## 1.1 In Columns

- df_exams['column_name'].sum()             #to sum of a column
- df_exams['column_name'].count()           #to count total number of rows
- df_exams['column_name'].mean()            #to find mean
- df_exams['column_name'].std()             #to find standard deviation of that column
- df_exams['column_name'].max()             #to find max in that column
- df_exams['column_name'].min()             #to find min in that column

- df_exams['column_name'].describe()        #a faster way to do all that in one-line

- df_students['gender'].value_counts() #this counts total number of gender in the 'gender' column. value_counts(normalize=true) gives the decimal value of the percentage of the count.
- 

## 1.2 In Rows

- df_exams['col1'] + df_exams['col2'] + df_exams['col3']             #to find the sum of the rows
- ((df_exams['col1'] + df_exams['col2'] + df_exams['col3']) /3).round(2)             #to find the sum of the rows

# Sort a Dataframe

- df.sort_values(by='age')                  #this sorts the dataframe by 'age' column
- df.sort_values(by='age', ascending= False)    #this sorts the dataframe by 'age' column in ascending order
- df.sort_values(by=['age', 'name'])        #this sorts the dataframe by multiple column 'age' and 'name'
- df.sort_index(ascending=False)            #this sorts the dataframe by index

- df.sort_column(by='age', inplace=True)            #without inplace, this method returns a copy of the dataframe without mutating the original dataframe

# Rename in Dataframe

- df.rename(columns = {"old_name": "new_name"})             #renaming one column
- df.rename(index = {0: "row1", 1: "row2"})                 #renaming the index values
- df.rename(columns = {"name": "Name", "age": "Age"})       #Multiple column rename at once
- df.columns = ["Name", "Age", "City"]              #this renames all the column in the given order. Length must be same

- df.index.name = "ID"                              #this labels the index column

# Pull data from URL

- df = pd.read_csv('url')

# Filter by one or multiple columns

- df[df["age"] > 20]                        # this filters dataframe where age is greater than 20
- df[(df["age"] > 20) & (df["city"] == "Delhi")]                # this filters dataframe where age is greater than 20 and city is Delhi
- df[(df["age"] > 20) | (df["city"] == "Mumbai")]               # this filters dataframe where age is greater than 20 or city is Mumbai

# np.where()

- import numpy as np

    df["status"] = np.where(df["age"] > 18, "Adult", "Minor")           # this creates a conditional column whose values are according to the condition

- df["grade"] = np.where(df["marks"] > 90, "A",
              np.where(df["marks"] > 75, "B", "C"))

# np.select()

- conditions = [
    df["marks"] > 90,
    df["marks"] > 75                                            # this is an advanced way, alternative of np.where(), for creating column of multiple conditions and values
]

choices = ["A", "B"]

df["grade"] = np.select(conditions, choices, default="C")

# isin()

- df[df["city"].isin(["val1", "val2"])]                      # this is an advanced way for filtering columns by multiple conditions

# duplicated()

- df["city"].duplicated(["Col1", "Col2"])                      # this is to find duplicates in a dataset. It returns boolean
- df["city"].duplicated(["Col1", "Col2"], keep='first')         # keeps the first duplicate as true. 'last' keeps the last duplicate as true. default is 'first'

# drop-duplicates()
- df["city"].drop-duplicates(["Col1", "Col2"]) # this is to delete duplicates in a dataset. It returns the dataset with non-duplicate values. It has same attributes as duplicated
- df["city"].drop-duplicates(["Col1", "Col2"], keep = 'first', ignore_index=True) # to ignore original index and start from starting. default is false


## Select rows/columns/cells in a dataset

# loc   (selecting names)
- df.loc[['rows_name'], ['column_name']]                #selecting rows and columns in a dataset
- df.loc[:, ['column_name']]                #selecting all rows and certain columns in a dataset
- df.loc[['rows_name'], :]                #selecting certain rows and all columns in a dataset
- df.loc['row_name', 'col_name']           # selecting a column and a row results in selecting a cell

# iloc  (selecting indexes)
- df.iloc[0:14, 1:7]                #selecting rows and columns via indexes in a dataset
- df.iloc[:, 4]                #selecting all rows and certain columns via indexes  in a dataset
- df.iloc[4, :]                #selecting certain rows and all columns via indexes in a dataset
- df.iloc[0, 1]           # selecting a column and a row results via indexes in selecting a cell

## Set a value in a dataset

- df.loc[['rows_name'], ['column_name']] = val                #sets the value in selected rows and columns in a dataset
- df.loc[:, ['column_name']] = val                #sets the value in selected all rows and certain columns in a dataset
- df.loc[['rows_name'], :] = val                #sets the value in selected certain rows and all columns in a dataset
- df.loc['row_name', 'col_name'] = val           # sets the value in selected cell

condition = df['col_name'] > condition_val
- df.loc[condition, ['columns']] = val              # sets the value conditionally. sets the values where the condition is true

## drop a row or column in a dataset

`axis-1` = columns
`axis-0` = rows

- .drop() returns a copy so use inplace or set equlas with the df to save changes
- 
# Row
- df.drop('A', axia=0, inplace=True)                  #this drops the row with index name as 'A'
- df.drop(index = [1], inplace=True)                  #this drops the row with index val as '1'

# Columns
- df.drop('column_name', axis=1, True)                  #this drops the column by column_name
- df.drop(columns = ['column_name'], inplace = True)    #this drops the column by column_name using colum attribute. axis is not required

# sample()

- df.sample(n: int | None = ..., frac=int | float | None, replace:bool = False, random_state=int, ignore_index: bool = False)

note while giving frac val more than 1 we have to set replace = True

# query() — SQL-style filtering 🧠

df.query("age > 20")
df.query("age > 20 and city == 'Delhi'")
df.query("age > 20 or city == 'Mumbai'")
city = "Delhi"
df.query("city == @city")
df.query("`total sales` > 1000")    #columns with spaces

# astype() — change data types 🔧

df["age"] = df["age"].astype(int)
df = df.astype({
    "age": "int",
    "salary": "float"
})


# apply() — run function on data ⚡

df["age"].apply(lambda x: x + 1)
df.apply(lambda row: row["age"] + row["salary"], axis=1)

df["status"] = df["age"].apply(lambda x: "Adult" if x > 18 else "Minor")
df["total"] = df.apply(
    lambda row: row["price"] * row["quantity"],
    axis=1
)               # Multiple columns

df["name"] = df["name"].apply(lambda x: x.upper())      # string manipulation

## all dataframe core attributes and methods

| Category        | Attribute / Method        | What it does |
|----------------|--------------------------|-------------|
| BASIC INFO     | df.shape                 | (rows, columns) |
|                | df.size                  | total elements |
|                | df.ndim                  | number of dimensions |
|                | df.index                 | row labels |
|                | df.columns               | column names |
|                | df.dtypes                | datatype of each column |
|                | df.values                | numpy array of data |
|                | df.axes                  | [index, columns] |

| INSPECTION     | df.head()                | first 5 rows |
|                | df.tail()                | last 5 rows |
|                | df.sample(n)             | random rows |
|                | df.info()                | summary + memory |
|                | df.describe()            | stats summary |
|                | df.memory_usage()        | memory per column |

| SELECTION      | df["col"]                | select column |
|                | df[["c1","c2"]]          | multiple columns |
|                | df.loc[]                 | label-based selection |
|                | df.iloc[]                | index-based selection |
|                | df.at[]                  | fast single value (label) |
|                | df.iat[]                 | fast single value (index) |

| FILTERING      | df.query()               | SQL-like filter |
|                | df[df["col"] > x]        | boolean filter |
|                | df.isin()                | match multiple values |
|                | df.where()               | conditional replacement |

| SORTING        | df.sort_values()         | sort by column |
|                | df.sort_index()          | sort by index |

| CLEANING       | df.drop()                | remove rows/columns |
|                | df.dropna()              | remove nulls |
|                | df.fillna()              | fill nulls |
|                | df.replace()             | replace values |
|                | df.rename()              | rename columns/index |
|                | df.astype()              | change datatype |

| DUPLICATES     | df.duplicated()          | find duplicates |
|                | df.drop_duplicates()     | remove duplicates |

| APPLY/TRANSFORM| df.apply()               | apply function |
|                | df.applymap()            | element-wise apply |
|                | df.map()                 | series mapping |
|                | df.transform()           | transform values |

| GROUPING       | df.groupby()             | group data |
|                | df.agg()                 | aggregate |
|                | df.size()                | count per group |
|                | df.mean()/sum()/count()  | stats ops |

| MERGING        | pd.merge()               | SQL join |
|                | df.join()                | join on index |
|                | pd.concat()              | stack data |

| INDEXING       | df.set_index()           | set index |
|                | df.reset_index()         | reset index |
|                | df.reindex()             | change index |

| ITERATION ⚠️   | df.iterrows()            | loop rows (slow) |
|                | df.itertuples()          | faster row loop |

| EXPORT         | df.to_csv()              | save CSV |
|                | df.to_excel()            | save Excel |
|                | df.to_json()             | save JSON |

| IMPORT         | pd.read_csv()            | load CSV |
|                | pd.read_excel()          | load Excel |
|                | pd.read_json()           | load JSON |

Game-Changers

| Feature            | Why it's powerful |
|-------------------|------------------|
| df.query()        | Cleaner than boolean masks |
| df.groupby()      | Core of analytics |
| df.merge()        | SQL joins in Python |
| df.apply()        | Custom logic |
| df.astype()       | Fix broken data instantly |
| df.isin()         | Multi-value filtering |
| df.value_counts() | Quick frequency |
| df.unique()       | Distinct values |
| df.nunique()      | Count uniques |
| df.corr()         | correlation matrix |
| df.pivot_table()  | Excel pivot killer |
| df.melt()         | reshape wide → long |
| df.explode()      | expand lists into rows |

cheat-sheet

Inspect → head(), info()
Select → loc, iloc
Filter → query(), boolean
Clean → dropna(), fillna()
Transform → apply(), astype()
Analyze → groupby()
Combine → merge(), concat()
Export → to_csv()

## dropna() — remove missing values 🧹

df.dropna()

df.dropna(axis=1)       # this drops columns with null

df.dropna(subset=["age"])       # Drops if specific column has null

df.dropna(thresh=2)             # Keeps rows with at least X non-null values

## pivot() — reshape (no aggregation)

df.pivot(index="date", columns="city", values="sales")      # if duplicates then error

## pivot_table() — pivot + aggregation 🔥

df.pivot_table(
    index="date",
    columns="city",
    values="sales",
    aggfunc="sum"
)

- Other aggfunc:

aggfunc="mean"
aggfunc="count"
aggfunc="max"

- Multiple aggregation
``` python
df.pivot_table(
    index="city",
    values="sales",
    aggfunc=["sum", "mean"]
)
```
# 🔥 When to use what
`pivot()` → clean data, no duplicates

`pivot_table()` → real-world messy data

## plot()

df.plot()

df.plot(kind="line")

df.plot(kind="bar")

df["age"].plot(kind="hist")

- Plot after pivot

    ``` python
    pivot_df = df.pivot_table(
        index="date",
        columns="city",
        values="sales",
        aggfunc="sum"
    )

    pivot_df.plot(kind="bar")
```

<!-- piechar, boxplot -->