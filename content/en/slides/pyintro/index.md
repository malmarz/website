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


## PyIntro
### Python Introduction for Researchers

Mohammad AlMarzouq

---

### Disclaimer
- This course will not make you an expert
- Gives you a lay of the land
- Proficiency comes with practice
- Assumes basic programming knowledge

---

# Important Notes
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
  - Allows you to execute python in different modes
    - Including notebooks
  - Well integrated with Git/Github
    - Can run in the cloud on `vscode.dev`
    - Try replacing `github.com` with `github.dev` in the URL for any repo
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

## Things to Know Before Starting

- Python Zen
- PEP8
- Idiomatic Python
- Handy References
  - https://www.pythoncheatsheet.org/
  - Hitchhikers guide to python
  - https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf
- Python 2 vs Python 3

---

## Basic Syntax
- Variables
- Data Types/Data Structures
- Operators
- Control Flow
- Functions
- Classes

---

## Installing Libraries

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


## Pandas Data Structures

Introduction to Series and DataFrame
Creating a Series and DataFrame
Accessing and modifying data in Series and DataFrame

## Loading Data

Loading data from CSV files
Loading data from Excel files
Loading data from SQL databases

## Saving Data

Saving data to CSV files
Saving data to Excel files
Saving data to SQL databases

## Data Cleaning

Handling missing data
Removing duplicates
Renaming and replacing

## Data Analysis

Descriptive statistics
Grouping and aggregating data
Correlation and covariance

## Data Visualization

Plotting with Matplotlib
Plotting with Seaborn

## Reshaping Data

Pivoting data
Melting data
Concatenating and merging data

## Statistical Analysis with Statsmodels

Introduction to Statsmodels
Simple linear regression
Multiple linear regression

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


