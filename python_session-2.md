##Python session - 2

##Aim of this session: 

Control flow: automating repeated boring tasks using loops rather than actively commanding Python to do stuffs (print, add etc.)

Control-flow allows Python to take a decision and do different things depending on different situations using `if/else statements` or `for loops`

###if loop

The `if-statement` is used to check a condition as true or false
- if the condition is true, block of codes inside the if statement (starts with a tab or four spaces) will be executed

The code below checks if the value of temperature is greater than 25 (degree). Since it's true for the block of code below, Python executes it
```
temperature = 26
if temperature > 25:
    print("Nice weather!")
```

If we change the value of temperature to 20, the if-statement becomes false and Python does not further read the codes that belong the if-statement 
```
temperature = 20
if temperature > 25:
    print("Nice weather!")
```

###if/else loop

The `else-statement` allows Python to read and execute another block of code id the if-statement is false

```
temperature = 20
if temperature > 25:
    print("Nice weather!")
else:
    print("Winter is coming!")
```

Multiple conditions can be given by introducing `elif-statement`
```
temperature = 20
if temperature > 25:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("The temperature is 25 degree.")
```

####Excercise - 1

We can interact with the commandline/terminal using `input()`, try it out by giving a value to the temperature on the commandline
```
temperature = input()
````

Now try this block of code
```
temperature = input()
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
temperature = input()
if temperature >= 25 and temperature < 37:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("You gave a wrong value!")
```

Give temperature a value < 25 and check what happens if you replace 'and' with 'or'
Warning: English's 'or' and Python 'or' are not always same

####Excercise - 2

Some more useful use of if-statements

Check if a variable or data type exists (not empty)

```
my_list = []
if my_list:
    print("my_list if not empty!")
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
    print("{} does not contain {}".format(my_string, my_item)
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
temperature = input()
if temperature >= 25 and temperature <= 37: # checks if the value is between 24 and 37
    print("Nice weather!")
elif temperature < 25:                      # checks if the value is less than 25
    print("Winter is coming!")
else:
    print("You gave a wrong value!")        # prompts if the value is not numerical
```

####Excercise - 3

Given a list of items check if a certain item exists, else add that item to the list
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
my_item = "cheese"
if item not in shopping:
    shopping.append(item)
```

Flow-chart exercise will be added here


###For loop

Most often we carry out the same task repeatedly to extract/update information, for example reading each items in list or dict or reading several files of same file format. This can be easily done by `for-loops` or `for ... in ...:` statement is the most powerful way to tackle the repeated tasks.

Example - 1
```
#use range to create a list of values
for entry in ramge(1,5):
    print(entry*456)
```
Example - 2
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
for item in shopping:
  print(item)
```
Example - 3
```
shopping_dict = ['item-0': 'bread', 'item-1': 'potatoes', 'item-2': 'eggs', 'item-3': 'flour', 'item-4': 'rubber duck', 'item-5': 'pizza', 'item-6': 'milk']
for item in shopping:
  print(item)
```
Example - 4
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
extrashopping = ['cheese', 'flour', 'eggs', 'spaghetti', 'sausages', 'bread']
for item in extrashopping:
    if item not in shopping:
        shopping.append(item)
print(shopping) 
```

####Excercise - 4
(i) Change the program above to print out a message when a duplicate item is found. To do this, you could add another if statement to see if the item is in the list. Alternatively, you can add an else: clause to the existing if statement. This will be executed when the condition in the if statement is false.
```
```

(ii) The example illustrated above is not the only solution to adding items to a list, whilst checking for duplicates. From the three choices below, choose the version that would achieve the same goal:

a)
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
extrashopping = ['cheese', 'flour', 'eggs', 'spaghetti', 'sausages', 'bread']
for item in extrashopping:
    if item not in shopping:   
        print item, "is already in the list."
    else: 
        shopping.append(item)
print(shopping)
```
b)
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
extrashopping = ['cheese', 'flour', 'eggs', 'spaghetti', 'sausages', 'bread']
for item in extrashopping:
    if item in shopping:
        shopping.append(item)
    else: 
        print item, "is already in the list."
print(shopping)
```
c)
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
extrashopping = ['cheese', 'flour', 'eggs', 'spaghetti', 'sausages', 'bread']
for item in extrashopping:
    if item in shopping:
        print item, "is already in the list."
    else: 
        shopping.append(item)
print(shopping)
```
