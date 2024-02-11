---
title: PyIntro
summary: Python introduction for researchers
authors: []
tags: [python, research, methods]
categories: []
date: "2021-11-18T06:05:15Z"
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: simple
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  #   Available highlight themes listed in: https://highlightjs.org/static/demo/
  #   Use lower case names and replace space with hyphen '-'
  highlight_style: dracula

  diagram: true
  diagram_options:
    # Mermaid diagram themes include: default,base,dark,neutral,forest
    theme: forest

  # RevealJS slide options.
  # Options are named using the snake case equivalent of those in the RevealJS docs.
  reveal_options:
    rtl: false
    controls: true
    progress: true
    slide_number: c/t  # true | false | h.v | h/v | c | c/t
    center: true
    mouse_wheel: true
    transition: concave  # none/fade/slide/convex/concave/zoom
    transitionSpeed: default  # default/fast/slow
    background_transition: slide  # none/fade/slide/convex/concave/zoom
    touch: true
    loop: false
    menu_enabled: true
    chalkboard_enabled: true
    history: true
  
---


## PyIntro for Researchers

### Mohammad AlMarzouq

ISOM Department

mo.almarzouq@ku.edu.kw

https://malmarz.netlify.app/en/courses/pyintro/

---

### Submit Your Research Papers

- Arab Journal of Administrative Sciences
- https://journals.ku.edu.kw/ajas
- [Call for papers](https://journals.ku.edu.kw/ajas/index.php/ajas/callforpapers)
- [Call for reviewers](https://journals.ku.edu.kw/ajas/index.php/ajas/creviewer)
- Quick turnaround time
- Open access
- Counts towards your promotion at KU

---

### Disclaimer
- This course will not make you an expert
- Gives you a lay of the land
- Proficiency comes with practice
- Assumes basic programming knowledge

---

### Important Notes
- We issue commands in Terminal and Python Console
- Will identify commands with a `$` or `>>>` prompt
- You should not type the prompt

---

### Outline

1. Why Python?
2. Why Not Python?
3. Development Environment
4. Hello World
3. Basic Syntax
4. Installing Libraries
5. Important Libraries
6. Introduction to Pandas
7. Reproducible Research
8. Final Thoughts

---

## Why Python
- General purpose programming language
- Cross platform
- High adoption
  - Especially in ML and Data Science
- Philosophy (Zen of Python)
- Documentation
- Thriving community
- Ecosystem
- Online resources and videos

---

## Python Philosophy
  ```python
  >>> import this
  ```

---

## Zen of Python
  - Beautiful is better than ugly.
  - Explicit is better than implicit.
  - Simple is better than complex.
  - Complex is better than complicated.
  - Readability counts.
---

## Zen of Python
  - There should be one-- and preferably only one --obvious way to do it.
  - Now is better than never.
  - Although never is often better than *right* now.
  - If the implementation is hard to explain, it's a bad idea.
  - If the implementation is easy to explain, it may be a good idea.
  - Namespaces are one honking great idea -- let's do more of those!

---

## Why NOT Python

- Already invested in another language/tool
- Network
- Learning curve
- Not sure where to start

---

## Development Environment

- Numerous tools and python distributions
  - Can get overwhelming
- Required 
  - Python Interpreter to execute code
  - Editor to write code 
  - Modern tools integrate both seamlessly
- Good news, you setup the environment once
  
---

### Writing Code
- Any Text Editor, including notepad
- Alternatives provide more features
  - Syntax Highlighting
  - Code Completion
  - Debugging
  - Version Control
  - Integration with other tools

---

### Executing Code
- Local vs Cloud
- Execution Modes
  - Script Mode
  - Interactive Mode
  - Hybrid/Notebook mode

---

### Python Interpreters
- Some OSs come with Python pre-installed
- Python.org
  - Most up to date
- Anaconda
  - Bundled with many libraries for data science
  - Easy to install and manage

---

### Local Code Editors
- VSCode
- RStudio
- Jupyter Notebook
- Jupyter Lab
- Sublime Text
- Atom
- Notepad++
- Vim/Emacs
- PyCharm
- Spyder

---

### Cloud Based Editors

- JupyterHub
- Github + mybinder
- Replit
- Kaggle
- Google Colab*
- CoCalc*
- Deepnote*

```verbatim
* Can be used to train and fine-tune DL models
```
---

### IDE of Choice

- VSCode
  - Likely to be part of your workflow for other languages/tasks
  - Extensions and copilot make it a powerful tool
  - Allows you to execute python in different modes, *even notebooks*
  - Well integrated with Git/Github
    - Replace `github.com` with `github.dev` in the URL for any repo
---

### VSCode Requirements for Python
- Install Python Interpreter
- Install Python Extensions for VSCode
- Install Libraries as needed

---

## Hello World

- Create a hello.py file
- Write the following code
```python 
print("Hello World")
```
- Run the code

---

### Things to Know Before Starting

- Python Zen
- PEP8 and Idiomatic Python
  - Writing and styling code the pythonic way
  - Great summaries at
    - [Python.org](https://www.python.org/dev/peps/pep-0008/)
    - [Real Python](https://realpython.com/python-pep8/)
    - [Hitchhikers guide to python](https://docs.python-guide.org/writing/style/)
- Python is case sensitive
- Python 2 vs Python 3

---

### Handy References

- [Python cheat sheet](https://www.pythoncheatsheet.org/)
- [Hitchhikers guide to python](https://docs.python-guide.org)
- [Pandas cheat sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)


---

### Overview of Basic Syntax
- Variables
- Data Types
- Operators
- Control Flow
- Functions
- Classes
- Collections
- Comprehensions

---
### Variables

- A name that refers to a value
- No need to declare type
  - Python is dynamically but strongly typed
  - Recent versions have type hints
- Can be reassigned

---

### Naming Conventions
- Lowercase
- Underscore to separate words
- Descriptive
- Avoid reserved words

---

### Variable Assignment
```python
x = 5
y = "Hello"
z = [1,2,3]
y = 10 # replaced value
```
---
### Some Useful Functions
- print()
- input()
- type()
- dir()
- help()

---

### Data Types
- int : 1, 2, 3
- float : 1.0, 2.0, 3.0
- str : "Hello", 'World', "1", "2"
- bool : True, False
- None 

---

### Collections
- list : [1,2,3]
- tuple : (1,2,3)
- set : {1,2,3}
- dict : {"a":1, "b":2, "c":3}

---
### Type Conversion
- int()
- float()
- str()
- bool()
- list()
- tuple()
- set()
- dict()

---

### Type Conversion Example
```python
x = "5"
y = int(x)
z = float(x)
```
- Does x equal y?
- Will throw an error if value cannot be converted

---


### Arithmetic Operators
| Precedence | Operator | Description |
|------------|----------|-------------|
| 1 | `()` | Parentheses |
| 2 | `**` | Exponentiation |
| 3 | `+x`, `-x`, `~x` | Unary plus, Unary minus, Bitwise NOT |
| 4 | `*`, `/`, `//`, `%` | Multiplication, Division, Floor division, Modulus |
| 5 | `+`, `-` | Addition, Subtraction |

---

### Bitwise Operators
| Precedence | Operator | Description |
|------------|----------|-------------|
| 6 | `<<`, `>>` | Bitwise shift operators |
| 7 | `&` | Bitwise AND |
| 8 | `^` | Bitwise XOR |
| 9 | `\|` | Bitwise OR |

---

### Comparison and Logical Operators
| Precedence | Operator | Description |
|------------|----------|-------------|
| 10 | `==`, `!=`, `<`, `<=`, `>`, `>=` | Comparisons, Equality, Inequality |
| 11 | `not` | Logical NOT |
| 12 | `and` | Logical AND |
| 13 | `or` | Logical OR |

---

### Creating Collections
```python
x = []
y = [1,2,3]
z = [1,2,3 ,["foo", "bar"]]

```
---
### Creating Collections

```python
x = {}
y = set()
z = {"a":1, "b":2, "c":3}
k = {1,2,3,4,4,5}

```

### Accessing Collections
- Indexing
- Slicing
- Iterating

---

### Indexing
- Used to fetch a single element
- 0 based
- Negative indexing
- Out of range indexing

---

### Example
```python
x = [1,2,3,4,5]
print(x[0])
print(x[-1])
print(x[5])
```

---

### Slicing
- Used to fetch a range of elements
- Start, Stop, Step
- Default values
- Negative slicing

---

### Example
```python
x = [1,2,3,4,5]
print(x[0:3])
print(x[:3])
print(x[3:])
print(x[::2])
print(x[::-1])
```

---

### Iterating
- for loop
- while loop
- list comprehension
- generator expression

---

### For Example
```python
x = [1,2,3,4,5]
for i in x:
  print(i) # this is a code block
```

---
### Code Blocks in Python
- Some statements are followed by a code block
- Such statements end with a colon `:`
- Example: if, for, while, def, class, with, try, except, finally
- Code blocks are defined by indentation
- Indentation is typically 4 spaces
- Will get back to this later

---

### Code Block Example
```python

def function():
  # do something
```

---

### Another Example
```python

if condition:
  # do something
  # do something else
if another_condition:
    # do something
else:
  # do something else
  # do something else
```


---

### Another Example
```python

if condition:
  # do something
  # do something else
  if another_condition:
    # do something
  else:
    # do something else
else:
  # do something else
  # do something else
```
---

### Another Example

```python
for i in range(10):
  # do something
  # do something else
  if i % 2 == 0:
    # do something
  else:
    # do something else
if condition:
  # do something
else:
  # do something else
```


---

### Back to Our For Example
```python
x = [1,2,3,4,5]
for i in x:
  print(i) 
```
---

### Another For Example
```python
x = [1,2,3,4,5]
for i in range(len(x)):
  print(x[i])
```

---

### While Example
```python
x = [1,2,3,4,5]
i = 0
while i < len(x):
  print(x[i])
  i += 1
```

---

### Filtering Using For Loops
```python
x = [1,2,3,4,5]
y = []
for i in x:
  if i % 2 == 0:
    y.append(i)
print(y)
```

---

### List Comprehension
```python
x = [1,2,3,4,5]
y = [i for i in x if i % 2 == 0]
print(y)
```

---

### Comprehensions

- Exist for lists, sets, and dictionaries
- Used to create new collections from existing ones
- Can be used to filter, transform, or combine collections
- Can be nested
- More efficient than loops

---

### Generator Expressions
- Similar to list comprehensions
- Use parentheses instead of square brackets
- Lazy evaluation
- More memory efficient
- Can be used to create infinite sequences
- Many functions in Python accept or return generator expressions
- Convert to list using `list()` to evaluate
- Otherwise, use in a for loop
---


### Control Flow

- Conditional Statements
  - if, elif, else
- loops
  - for, while

---

### If Statements

```python
if condition:
  # do something
elif condition: # optional
  # do something else
else: # optional
  # do something else
```

---

### Conditions

- Comparison operators
  - `==`, `!=`, `<`, `<=`, `>`, `>=`
- Logical operators
  - `and`, `or`, `not`
- Membership operators
  - `in`, `not in`
- Identity operators
  - `is`, `is not`
- Truthy and Falsy values

---
### Truthy and Falsy Values

| Value Type | Truthy | Falsy |
|------------|--------|-------|
| Boolean | `True` | `False` |
| Null |  | `None` |
| Zero |  | `0`, `0.0`, `0j` |
| Empty Collections |  | `""`, `()`, `[]`, `{}`, `set()`, `range(0)` |
| Others | Any other value not listed in Falsy |  |

---

### Functions

- A block of code that only runs when it is called
- Can take arguments
  - Mandatory or optional
  - Positional or keyword
- Can return values
- Great for scoping variables
  - Avoids global variables
  - Makes code more modular
---

### Void Function Example
```python
def my_function():
  print("Hello from a function")
```
- This is just a definition, the function is not executed
- To  execute:

```python
my_function()
```

---

### Function with Arguments
```python
def my_function(name):
  print("Hello " + name)
```

---

### Function with Return Value
```python
def my_function(x):
  return x**2

# execute
print(my_function(2))
```

---

### Function with Default Argument
```python
def my_function(x=2):
  return x**2

# execute
print(my_function()) # Where is the argument?
```

---

### Function with Keyword Arguments
```python
def my_function(x=2, y=3):
  return x**y

# execute
print(my_function(y=2, x=3))
# or
print(my_function(x=3, y=2))
```

### Other Ways to Call The Functions

```python
print(my_function(3, 2)) # positional
# or
print(my_function(x=3)) # keyword
# or
print(my_function(y=3))
# or
print(my_function())
```
What are the arguments?
---

### Function with Variable Arguments
```python
def my_function(*args):
  return sum(args)

# execute
print(my_function(1,2,3,4,5))
print(my_function(1,2,3))

```

---

### Function with Variable Keyword Arguments
```python
def my_function(**kwargs):
  return kwargs

# execute
print(my_function(a=1, b=2, c=3))
print(my_function(x=1, y=2))

```

---  

### Things to Note
- `args` and `kwargs` are just names
- `args` is a tuple
- `kwargs` is a dictionary
- `args` and `kwargs` are optional and must be at the end
  - `args` (positional) before `kwargs` (keyword)
- `args` and `kwargs` can be used together

---

### Variables Vs. Functions

- Variables store values
- Functions store instructions
- Both are considered variables that you can refer to
- Use parentheses to execute variables containing functions

---
### What's The Output?
```python
print(x)
print("x")
print(input)
print(input())
```
---
### Challenge

- Rename print to z
- Redefine print to be input

---

### Solution

```python
z = print
z("hello world")
print("Hello world")
print = input
print("Hello world")
```
---

### Python Can Do Tricks
- But why is this useful?
- It means you can 
  - Pass functions as arguments to other functions
  - You can return functions from other functions
  - You can store functions in data structures
  - You can create functions on the fly
  - You can create functions that create functions
- Code flexibility
---

### Results In Some Very Useful Features
- Lambda Functions
- Decorators
---

### Example Lambda Function

```python
f = lambda x: x**2
print(f(2))
```
---


### More Useful Example

```python
num_list = [1,2,3,4,5]

# in just one line
squared = list(map(lambda x: x**2, num_list))
```
----

### Alt Solution
```Python
num_list = [1,2,3,4,5]

# Three lines of code
def f(x):
  return x**2

squared = list(map(f, num_list))
```

---

### Classes

- A blueprint for creating objects
- Objects have properties and methods
- Will not cover in this session
  - Requires we cover OOP
- Instead, we will focus on using classes
  - Many libraries provide classes

---

### Using Classes

- You must create an instance of the class
- You can then use the methods and properties from the instance
- You can create multiple instances of the same class
- Each instance will have its own properties
  - Methods will work on the properties of the instance
  - Another way to scope variables

---

### Example of Using Classes

```python
import pandas as pd
df = pd.DataFrame({"col1": [1,2,3]}) # instance
df2 = pd.DataFrame({"A": [4,5,6]}, {"B": [7,8,9]}) # another instance

# calling a method
df.head()
df2.head()

# accessing a property
df.columns
df2.columns
```



---

## Break
- Resume in 15 minutes
- Make sure pandas library is installed
- See next few slides for instructions

---

### Python Libraries
- Built-in
  - Comes with Python
- Third-party
  - Installed using pip

---

### Using Libraries
- Import the library
- Read documentation to understand how to use the library
  - You can peak into libraries using `dir()` and `help()`
- Use the library

---

### Example of Using Libraries
```python
import math #simple import

# calling a library function
math.sqrt(4)
```

Always prefix the function with the library name

---

### Another Example

```python

from math import sqrt # import a specific function

# calling the function
sqrt(4)
```

---

### Bad Example (Avoid This)

```python
from math import * # import everything

# calling the function
sqrt(4)
```
Risk of overwriting functions

---

### Example of Aliasing Libraries

```python
import pandas as pd # aliasing

# calling a function/class
pd.DataFrame()
```
Conventional for most data science libraries

---

## Installing Libraries

```bash
$ pip install pandas
```
**Remember**: This is a command line command

---


## Important Libraries

https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

numpy
scipy
sklearn
matplotlib
seaborn
plotly
altair
statsmodels
pandas
networkx
pydot
tensorflow
pytorch
keras
nltk
spacy
gensim
tomotopy
scrapy
beautifulsoup
pymc
dowhy
econml
GROBID


---



---

## Introduction to Pandas

---

### What is Pandas?
- Open source data analysis and manipulation tool
- Built on top of the Python programming language
- Offers data structures and operations for manipulating numerical tables and time series
- Integrates well with other libraries in Python ecosystem

---

## Installation and Setup

---

### How to install Pandas

```bash
pip install pandas
```
Anaconda python comes with Pandas and other libraries pre-installed.

---

### Importing Pandas in your script

```python
import pandas as pd # conventional alias

```

Setup and configuration typically done at top of script or notebook

---


### Typical Research Setup

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import statsmodels.api as sm
import sklearn
```

---

## Pandas Data Structures

Introduction to Series and DataFrame
Creating a Series and DataFrame
Accessing and modifying data in Series and DataFrame
---

## Loading Data

Loading data from CSV files
Loading data from Excel files
Loading data from SQL databases

---

## Saving Data

Saving data to CSV files
Saving data to Excel files
Saving data to SQL databases

---

## Data Cleaning

Handling missing data
Removing duplicates
Renaming and replacing

---

## Data Analysis

Descriptive statistics
Grouping and aggregating data
Correlation and covariance

---

## Data Visualization

Plotting with Matplotlib
Plotting with Seaborn

---

## Reshaping Data

Pivoting data
Melting data
Concatenating and merging data

---

## Statistical Analysis with Statsmodels

Introduction to Statsmodels
Simple linear regression
Multiple linear regression

---

## ML with Scikit-learn

Introduction to Scikit-learn
Supervised learning
Unsupervised learning


---


## Reproducible Research

---

## Final Thoughts
- Use Python to become proficient
- https://software-carpentry.org/lessons/


