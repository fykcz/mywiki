# Pandas a podobny
https://levelup.gitconnected.com/stop-using-pandas-for-everything-85ba2886c3d4

## Polars
Polars is optimized for blazing-fast performance on large datasets.

**When to use:**
* Processing huge CSVs or Parquet files.
* Running complex queries which require serious optimization.
* When you’re tired of how slow Pandas’ groupby is.
## Dask
It is designed for the datasets that don’t fit into memory to chunk up computations across multiple cores or, preferably, even multiple machines.

**When to use it:**
* Working with datasets bigger than your RAM.
* The deployment of analyses on distributed systems or cloud environments.
* Training machine learning models based on big data.
## Vaex
Specialised in out-of-core operations, it can process datasets with billions of rows — yes billions — on a laptop.

**When to use it:**
* Exploratory data analysis for large datasets.
* Visualization of data with no need to write 10 lines of code in Matplotlib.
* Avoid the Dreaded “MemoryError” in Pandas.
## Modin
It is a drop-in parallel replacement for pandas that allows you to get away with writing much faster code.

**When to Use It:**
* You know Pandas inside out but need faster performance.
* Migrating old Pandas-based projects to a scalable solution.
## PySpark
Though overkill for small data sets, it tends to make sense in a regime of distributed computing with rather big data pipelines.

**When to use it:**
* Building ETL pipelines for production systems.
* Analyzing log files or streaming data.
* Working in environments where scalability is non-negotiable.
# Why Developers Are Ditching PostgreSQL, MySQL and MongoDB
https://aws.plainenglish.io/why-developers-are-ditching-postgresql-mysql-and-mongodb-b3b953ebe6b6

## Milvus
Open-source vector database designed to power AI applications and similarity search at massive scale.

**When to Use Milvus**
* Image and video search
* Recommendation systems
* Natural language processing applications
* Fraud detection

## InfluxDB
InfluxDB is a purpose-built time series database designed for high-performance handling of timestamped data.

**When to Use InfluxDB:**
* Real-time analytics applications
* IoT data monitoring
* System monitoring and metrics collection

## Neo4j
Neo4j is a graph database that uses nodes, edges, and properties to represent and store data. This structure is ideal for applications where relationships between entities are crucial.

**When to Use Neo4j**
* Social network analysis
* Recommendation engines
* Fraud detection systems
* Knowledge graphs

## DuckDB
It’s designed for fast analytical queries, particularly in data science workflows, and can seamlessly integrate with pandas DataFrames.

**When to Use DuckDB**
* Data analysis and exploration
* ETL processes
* **Embedded analytics in Python applications**

## Redis
Redis is a fast, in-memory data structure store that can be used as a database, cache, and message broker.

**When to Use Redis**
* Caching layer for performance improvement
* Real-time analytics
* Session management
* Leaderboards and counting

## Tile38
Tile38 is a specialized geospatial database that allows you to store, query, and analyze geospatial data in real-time. It’s ideal for applications such as fleet management, asset tracking, and location-based services.

**When to Use Tile38**
* Fleet management systems
* Location-based services
* Asset tracking
* Geofencing applications

# Essential for Lazy Developers: Five Efficient Python Decorators
https://faun.pub/essential-for-lazy-developers-five-efficient-python-decorators-a8d5964994f8

# 10 Ways to Write Better Python Codes
https://levelup.gitconnected.com/10-ways-to-write-better-python-codes-55fc862ab0ef

## 1. Using “Generators” to Save Memory
```python
def process_large_file(file_path):
    """
    Generator function to read a large file line by line.
    """
    with open(file_path, 'r') as file:
        for line in file:
            yield line  

# Specify the path to your large file
log_file_path = 'path/to/your/large_file.txt'

# Use the generator to process the large file line by line
for line in process_large_file(log_file_path):
    print(line.strip())  # .strip() removes any extra whitespace or newline characters
```

## 2. Using ".setdefault()" in Dictionaries
```python
# Initial inventory
inventory: dict[str, int] = {"jeans": 500, "top": 600}     
              
# Add more products with default stock levels if they are not already present
products_to_add: list[str] = ["skirt", "shirt", "tee"]

for product in products_to_add:
    inventory.setdefault(product, 500)

# Print the final updated inventory
print("Final updated inventory:", inventory)

"""
# Output:
Final updated inventory: {'jeans': 500, 'top': 600, 'skirt': 500, 'shirt': 500, 'tee': 500}
"""
```

## 3. Using Dictionaries to avoid "if-elif" hell
```python
from collections.abc import Callable

# Function 1 
def first():
======print====(===="Calling First Function..."====)==


# Function 2
def second():
  print("Calling Second Function...")


# Function 3
def third():
  print("Calling Third Function...")


# Function Default
def default():
  print("Calling Default Function...")

# User Input
options: int = int(input("Enter an option :", ))

# Dictionary to hold options as key and functions as values  
funcs_dict : dict[int, Callable[[], None]] = {1: first, 2: second, 3: third}

# Checking if the key exist and incase it doesn't then deafult function will run
final_result = funcs_dict.get(options, default)
final_result()
```

## 4. Using "Counter" from Collections Module
```python
from collections import Counter
import re

# Read the text file
with open("sample_text.txt", "r") as file:
  text = file.read()

# Clean and Tokenize the text
cleaned_text: str = re.sub(r'[^\w\s]', '', text.lower().split())

# Use Counter() to count the words
word_counts: Counter = Counter(cleaned_text)

# Printing second highest most common word 
most_commmon = counter.most_common(2) # passed in Number will denotes how many common numbers we want (counting starts from 1-n)
print("Second Most Common Word is: ", most_commmon[0]) # print in zeroth index element from 2 most common ones

"""
# Output:
Second Most Common Number is: ('data', 82)
"""
```

## 5. Using "Memoization" to Optimize Code
```python
import time

def memo_fibonacci(num: int, dictionary: dict[int, int]):
    if num in dictionary:
        return dictionary[num]
    else:
        dictionary[num] = memo_fibonacci(num-1, dictionary) + memo_fibonacci(num-2, dictionary)
        return dictionary[num]

# Catching using a Dictionary
dictionary: dict[int, int] = {0: 1, 1: 1}

# Elapsed time
start_time: float = time.time()
# Calling the function
result: int = memo_fibonacci(48, dictionary)
end_time: float = time.time()
# Calculating the elapsed time
elapsed_time: float = end_time - start_time


print(f"Result: {result}") # Result: 7778742049
print(f"Elapsed time: {elapsed_time:.6f} seconds") # Elapsed time: 0.000133 seconds
```

## 6. Using "@decorators" to avoid Repetitiveness
```python
import time

def elapsed_time(func):
    def wrapper():
        start_time: float = time.time()
        
        func()
        
        end_time: float = time.time() - start_time
        print(f"{func.__name__}() took {end_time:.6f} seconds")
        
    return wrapper

@elapsed_time
def some_code():
    # Simulating running code..
    time.sleep(0.00002)

# Calling the function
some_code() # some_code() took 0.000009 seconds
```

## 7. Using `dataclass` for Clean Data Structures
```python
from dataclasses import dataclass

@dataclass
class Employee:
    id_: int
    name: str
    salary: float

e1 = Employee(id_=1, name='Tusk', salary=69999.99)
print(e1) # Employees(id_=1, name='Tusk', salary=69999.99)
```

```python
from dataclasses import dataclass

@dataclass
class Employee:
    id_: int
    name: str
    salary: float

    def __repr__(self):
        return f"Employee(id_={self.id_}, name={self.name}, salary={self.salary})"

    def __str__(self):
       return f"{self.name} earns ${self.salary}."

e1 = Employee(id_=1, name='Tusk', salary=69999.99)
print(repr(e1))  # Employee(id_=1, name=Tusk, salary=69999.99)
print(str(e1))   # Tusk earns $69999.99.
```

## 8. Using "match" for Clean Input Handling
```python
from dataclasses import dataclass

# Defining a class using dataclass
@dataclass
class Point:
    x: int
    y: int

# Match statements to handle different cases
def where_is(point):
    match point:
        case Point(x=0, y=0):
            return ("Origin")
        case Point(x=0, y=y):
            return (f"Y={y}")
        case Point(x=x, y=0):
            return (f"X={x}")
        case Point(x, y):
            return("Somewhere else")
        # To catch anything else that the user inputs
        case _:
            return("Not a point")

# Examples
print(where_is(Point(0, 0)))   # Output: Origin
print(where_is(Point(0, 10)))  # Output: Y=10
print(where_is(Point(10, 0)))  # Output: X=10
print(where_is(Point(10, 10)))  # Output: Somewhere else
print(where_is("Not a point"))  # Output: Not a point
```

## 9(A). Using "all" Operator instead "and"
```python
# User input from a registration form 
form_data: dict[str, str] = {"name" : "Nikita", 
             "email": "analyticalnikita@gmail.com",
             "phone": "123478911"}

# List of reuired fields
required_fields: list[str] = ["name", "email", "phone"]

# Using all operator
if all(field in form_data for field in required_fields):
    print("All required fields are filled out.")
else:
    print("Some required fields are missing or empty.")

"""
# Output:
All required fields are filled out.
"""
```

## 9(B). Using "any" Operator instead "or"
```python
# List of permissions to the user
user_permission: list[str] = ["read", "execute"]

# Check if user has at least one of the required permissions
required_permissions: list[str] = ["write", "read", "admin"]
    
# Using "all" operator
if any(permission in user_permission for permission in required_permissions):
    print(f"Since you have required permissions. Access is allowed.")
else:
    print("You're a standard user. Not allowed the access.")

"""
# Output:
Since you have required permissions. Access is allowed.
"""
```

## 10. Using the Comprehensions for Shorter Syntax
#### 10(A). List Comprehensions
```python
# Nested-if using List Comprehension
fruits: list[str] = ["apple", "orange", "avacado", "kiwi", "banana"]
basket: list[str] = ["apple", "avacado", "apricot", "kiwi"]

[i for i in fruits if i in basket if i.startswith("a")] # ['apple', 'avacado']
```

#### 10(B). Tuple Comprehensions
```python
# Generator expression converted to a tuple
tuple(i**2 for i in range(10))

# (0, 1, 4, 9, 16, 25, 36, 49, 64, 81)
```

#### 10(C). Dictionary Comprehensions
```python
# Creating a list of apple names
apple_names: list[str] = ["apple", "pineapple", "green apple"]

# Creating a dictionary with apple names as keys and their lengths as values
print({apple_name: len(apple_name) for apple_name in apple_names})

# {"apple": 5, "pineapple": 9, "green apple": 11}
```

#### 10(D). Set Comprehensions
```python
# Creating a set with condition
print({i**2 for i in range(1, 11) if i > 5})

# {64, 36, 100, 49, 81}
```

# 14 pandas tricks you MUST know
https://medium.com/@deyprakash753/14-pandas-tricks-you-must-know-aee396dde875

## 1. Selecting Columns by Data Type
```python
df.select_dtypes(include=['float64', 'int64'])
```
## 2. Conditional Filtering with `query`
```python
df.query('age > 25 & city == "Mumbai"')
```
## 3. Chaining Operations with `pipe`
```python

def normalize(df):
    return (df - df.mean()) / df.std()

df.pipe(normalize)
```
## 4. Exploding a List-Like Column
Suppose you have a DataFrame where one column contains lists of tags or categories associated with each record. By exploding this column, you can create a row for each tag or category, making it easier to count, group, or analyze them separately.

```python
df.explode('column_with_lists')
```
## 5. Using `applymap` for Element-Wise Operations
```python
df.applymap(lambda x: len(str(x)) if isinstance(x, str) else x)
```
## 6. Creating New Columns with `assign`
```python
df.assign(total_cost=lambda x: x['price'] * x['quantity'])
```
## 7. Using `cut` to Bin Data
```python
df['age_group'] = pd.cut(df['age'], bins=[0, 18, 35, 60, 100], labels=['Teen', 'Young Adult', 'Adult', 'Senior'])
```
## 8. Memory Optimization with `astype`
```python
df['category_column'] = df['category_column'].astype('category')
```
## 9. Forward and Backward Filling Missing Data
In time series data, if you have missing values in a sequence and you want to fill them with the last known value (e.g., carrying forward the last stock price), `ffill` and `bfill` provide a simple and effective solution.
```python
df.ffill()  # Forward fill
df.bfill()  # Backward fill
```
## 10. Working with MultiIndexes
```python
df.set_index(['col1', 'col2'], inplace=True)
df.loc[('value1', 'value2')]
```
## 11. Aggregating Data with `groupby` and `agg`
```python
df.groupby('category').agg({'price': ['mean', 'sum'], 'quantity': 'sum'})
```
## 12. Reshaping Data with `melt`
Suppose you have monthly sales data for different products spread across multiple columns. `melt` can be used to convert these columns into a single 'Month' column, making the DataFrame longer and easier to work with for analysis.
```python
pd.melt(df, id_vars=['id'], value_vars=['A', 'B'], var_name='variable', value_name='value')
```
## 13. Pivoting DataFrames
If you have data in a long format, such as sales figures for different products and dates, and you want to create a table where each product has its own column and each row represents a date, `pivot` is the way to go.
```python
df.pivot(index='date', columns='product', values='sales')
```
## 14. Using `sample` for Random Sampling
```python
# Select 10% of the data randomly to explore a subset of a large dataset
sampled_df = df.sample(frac=0.1, random_state=42)
```

# Creating Amazing Visualizations with Python
https://riteshshergill.medium.com/creating-amazing-visualizations-with-matplotlib-and-seaborn-486fa7d68c1e

# 10 essential VS Code tips & tricks for greater productivity
* Enable local source control with **Timeline view**; available in Explorer pane by default.
* Autosave files with `File > Autosave`.
* Run commands in Command Palette with `Ctrl + Shift + P` or `Shift + Command + P`.
* Go to a file with `Ctrl + P`, navigate between open files with `Alt + Left/Right` or `Ctrl + Tab`.
* Go to a line with `Ctrl + G`.
* Delete a line with `Ctrl + Shift + K`
* Enable smooth typing with `Editor: Cursor Smooth Caret Animation` setting.
* Format code with Format Document command, use [**Prettier**](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode), change shortcut to `Ctrl + D, Ctrl + D`
* Use multiple cursors at once with `Alt + Click, Ctrl + Alt + Up/Down` adds one above/below
* Move a line up or down with **Alt/Option + Up/Down** in Windows/Mac
* Create a new file by double-clicking the Explorer pane or **set a custom keyboard shortcut**. Create a new file in a new folder with “**folder/file.ext**”

# Top GitHub Accounts Every Python Developer Should Follow
https://medium.com/@ccpythonprogramming/top-github-accounts-every-python-developer-should-follow-c5b2d142d93a
# Master Pandas to Build Modular and Reusable Data Pipelines
https://medium.com/@conalhenderson/master-pandas-to-build-modular-and-reusable-data-pipelines-1d12b003a423
# Use VS Code Like a Pro
https://javascript.plainenglish.io/use-vs-code-like-a-pro-53973daa534f
## Boost Your File Tree Visibility
Add these lines to `settings.json`
```json
{
  "workbench.tree.indent": 15,
  "workbench.tree.renderIndentGuides": "always",
  "workbench.colorCustomizations": {
    "tree.indentGuidesStroke": "#05ef3c"
  }
}
```
# Password Generator
```python
from random import choice
print(''.join([choice('abcdefghijklmnopqrstuvwxyz0123456789%^*(-_=+)') for i in range(10)]))

```
# 33 Mindblowing Python Code Snippets for Everyday Problems
https://medium.com/pythoneers/33-mindblowing-python-code-snippets-for-everyday-problems-056f4d37ff20