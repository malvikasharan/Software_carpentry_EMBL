##Python session - 2

##Aim of this session: 

Flow control: automating repeated boring tasks using loops rather than actively commanding Python to do stuffs (print, add etc.)

Flow control allows Python to take a decision and do different things depending on different situations using `if` or `else` statements or `for` loops

###if statements

The `if` statement is used to check a condition as __True__ or __False__
- if the condition is __True__, block of codes inside the if statement (starts with a tab or four spaces) will be executed

The code below checks if the value of temperature is greater than 25 (degree). Since it's __True__ for the block of code below, Python executes it
```
temperature = 26
if temperature > 25:
    print("Nice weather!")
```

If we change the value of temperature to 20, the if statement becomes __False__ and Python does not further read the codes that belong the if statement 
```
temperature = 20
if temperature > 25:
    print("Nice weather!")
```

###if/else statements

The `else` statement allows Python to read and execute another block of code id the if statement is __False__

```
temperature = 20
if temperature > 25:
    print("Nice weather!")
else:
    print("Winter is coming!")
```

Multiple conditions can be given by introducing `elif` statement
```
temperature = 20
if temperature > 25:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("The temperature is 25 degree.")
```

#### Exercise - 1

We can interact with the commandline/terminal using `input()`, try it out by giving a value to the temperature on the commandline
```
temperature = input()
```

Now try this block of code
```
user_input = input()  # input returns a "string"
temperature = int(user_input)  # convert from a "string" to an "int"
if temperature > 25:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("The temperature is 25 degree.")
```

Adding even more conditions (conditions inside conditions)
- Option - 1: not so elegant nested if statements
```
if ...:
    if ...:
    elif ...:
    ...
    else ...:
elif ...:
    if ...:
    elif ...:
    ...
    else ...:
elif ...:
    ...
else:
    ...
```

- Option - 2: connecting conditions by Boolean (and, or, not)
```
user_input = input()  # input returns a "string"
temperature = int(user_input)  # convert from a "string" to an "int"
if temperature >= 25 and temperature < 37:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("You gave a wrong value!")
```

Give temperature a value < 25 and check what happens if you replace 'and' with 'or'

#####Warning: English's *or* and Python's *or* are not always same#####

####Exercise - 2

Some more useful use of if statements

Check if a variable or data type exists (not empty)

```
my_list = []
if my_list:
    print("my_list is not empty!")
else:
    my_list.append("something")
    print("I added something to my_list")
```

Check if an item exists in a string (hint: if item in string:)...
```
my_string = "Whether you're new to programming or an experienced developer, it's easy to learn and use Python."
my_item = "Python"

if my_item in my_string:
    print(my_string)
else:
    print("{} does not contain {}".format(my_string, my_item))
```
...or does not exist

```
my_string = "Whether you're new to programming or an experienced developer, it's easy to learn and use Python."
my_item = "Perl"
if my_item not in my_string:
    print(my_string)
else:
    print("{} contains {}".format(my_string, my_item)
```

####Styling tip: annotate your codes so others can read and understand what your code is doing

```
""" 
This is a Docstring. 
This script gives its opinion on weather
"""
user_input = input()  # input returns a "string"
temperature = int(user_input)  # convert from a "string" to an "int"
if temperature >= 25 and temperature <= 37: # checks if the value is between 24 and 37
    print("Nice weather!")
elif temperature < 25:                      # checks if the value is less than 25
    print("Winter is coming!")
else:
    print("You gave a wrong value!")        # prompts if the value is not numerical
```

####Exercise - 3

Given a list of items check if a certain item exists, else add that item to the list
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
my_item = "cheese"
if item not in shopping:
    shopping.append(item)
```

Flow-chart exercise will be added here


###For loop

Most often we carry out the same task repeatedly to extract/update information, for example reading each items in list or dict or reading several files of same file format. This can be easily done by `for` loops` or `for ... in ...:` statement is the most powerful way to tackle the repeated tasks.

Example - 1

```
#use range to create a list of values
for entry in range(1,5):
    print(entry*456)
```
Example - 2

```
shopping = ['bread', 'potatoes', 
            'eggs', 'flour', 
            'rubber duck', 'pizza', 
            'milk']
for item in shopping:
  print(item)
```
Example - 3

```
shopping_dict = {'item-0': 'bread', 'item-1': 'potatoes', 
                 'item-2': 'eggs', 'item-3': 'flour', 
                 'item-4': 'rubber duck', 'item-5': 'pizza', 
                 'item-6': 'milk'}
for item in shopping_dict:
  print(item, "is:", shopping_dict[item]) 
```
Example - 4

```
shopping = ['bread', 'potatoes', 
            'eggs', 'flour', 
            'rubber duck', 'pizza', 
            'milk']
extrashopping = ['cheese', 'flour', 
                 'eggs', 'spaghetti', 
                 'sausages', 'bread']
for item in extrashopping:
    if item not in shopping:
        shopping.append(item)
print(shopping) 
```

####Exercise - 4
(i) Change the program above to print out a message when a duplicate item is found. To do this, you could add another if statement to see if the item is in the list. Alternatively, you can add an else: clause to the existing if statement. This will be executed when the condition in the if statement is __False__
```
```

(ii) The example illustrated above is not the only solution to adding items to a list, whilst checking for duplicates. From the three choices below, choose the version that would achieve the same goal:

a)

```
shopping = ['bread', 'potatoes', 
            'eggs', 'flour', 
            'rubber duck', 'pizza', 
            'milk']
extrashopping = ['cheese', 'flour', 
                 'eggs', 'spaghetti', 
                 'sausages', 'bread']
for item in extrashopping:
    if item not in shopping:   
        print item, "is already in the list."
    else: 
        shopping.append(item)
print(shopping)
```
b)

```
shopping = ['bread', 'potatoes', 
            'eggs', 'flour', 
            'rubber duck', 'pizza', 
            'milk']
extrashopping = ['cheese', 'flour', 
                 'eggs', 'spaghetti', 
                 'sausages', 'bread']
for item in extrashopping:
    if item in shopping:
        shopping.append(item)
    else: 
        print item, "is already in the list."
print(shopping)
```
c)

```
shopping = ['bread', 'potatoes', 
            'eggs', 'flour', 
            'rubber duck', 'pizza', 
            'milk']
extrashopping = ['cheese', 'flour', 
                 'eggs', 'spaghetti', 
                 'sausages', 'bread']
for item in extrashopping:
    if item in shopping:
        print item, "is already in the list."
    else: 
        shopping.append(item)
print(shopping)
```

### Functions

Functions are the reusable  block of code that you define, and can be executed any number of times from different parts of any script(s) you write. This reusability is called "calling the function". 
Functions are highly important building blocks of any program.

You have been using built-in functions already, for example: len(), range(), sorted(), max(), min(), sum() etc.

#### Structure of writing a function:

* def (keyword) + function name (you choose) + (): 
* newline with 4 spaces or a tab +  block of code
* Call your function

#### Non parametric function

```
 def say_hi():
    print("hi")
```
    
#### Parametric function

```
def say_hi(name): # here name is a variable
    print("hi {}".format(name))
name = 'Greg''
say_hi(name)
```

#### Returning values
```
def say_hi(name): # here name is a variable
    greet = "hi {}".format(name)
    return greet

name = 'Greg'
print(say_hi(name))
```

#### Local Vs. global variable

```
def say_hi(name): # here name is a variable
    greet = "hi {}".format(name)    # greet is a local variable, this is known only inside a function
    return greet
current_greet = say_hi(name)        # current_greet is a global variable, known outside a function
print(current_greet)                # global variables can be further manipulated
```


### Exercises

#### Let"s take one of our older codes and write them in function


### Using Modules
One of the great things about Python is the free availability of a _huge_ number of modules that can be imported into your code and used. Modules are developed with the aim of solving some particular problem or providing particular, often domain-specific, capabilities.  
In order to import a module, it must first be installed and available on your system. We will cover this briefly later in the course.  
A large number of modules are already available for import in the standard distribution of Python: this is known as the standard library. If you installed the Anaconda distribution of Python, you have even more modules already installed.  
Importing a module is easy:

```
import numpy
array_one = numpy.array([1,2,3,4,5,6])
print(array_one)

import pandas
data = pandas.read_table()
data.plot()
```
#### Aside: Namespaces
Python uses namespaces a lot, to ensure appropriate separation of functions, attributes, methdos etc between modules and objects. When you import an entire module, the functions and classes available within that module are loaded in under the modules namespace - `pandas` in the example above.  
It is possible to customise the namespace at the point of import, allowing you to e.g. shorten/abbreviate the module name to save some typing:

```
import numpy as np
array_two = np.array([10, 11, 12, 13, 14])
print(array_two)

import pandas as pd
data = pd.read_table()
data.plot()
```
Also, as in the examples above, if you need only a single function from a module, you can import that directly into your main namespace (where you don't need to specify the module before the name of the function):

```
from numpy import array
array_three = array([1, 1, 2, 3, 5, 8])
print(array_three)

from pandas import read_table
data = read_table()
data.plot()
```

#### Conventions
- You should perform all of your imports at the beginning of your code. This ensures that
  - users can easily identify the dependencies of a program, and 
  - that any lacking dependencies (causing fatal `ImportError` exceptions) are caught early in execution
- the shortening of `numpy` to `np` and `pandas` to `pd` are very common, and there are others too - watch out for this when e.g. reading docs and guides/SO answers online.

### Exercises - Importing
```
--- numpy
series_a = numpy.array([5, 5, 5, 5, 5])
series_b = ---.array([1, 2, 3, 4, 5])
series_c = series_a - series_b
print(series_c)
```

```
import pandas --- pd
data = pd.read_table()
```

#### Aside: Your Own Modules
Whenever you write some python code and save it as a script, with the `.py` file extension, you are creating your own module. If you define functions within that module, you can load them into other scripts and sessions.

### Some Interesting Module Libraries to Investigate
- sys
- collections
- math
- argparse
- time
- datetime
- numpy
- scipy
- matplotlib
- pandas
- scikit-learn
- requests
- biopython
