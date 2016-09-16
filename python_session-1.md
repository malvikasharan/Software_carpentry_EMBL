#Python session - 1

##Aim of this session: 

Learn the basics (what is? how to?)

###Classic beginning with "Hello World!"

- Run Python (Type "python" + click run button)
- Print something
```
print('Hello World!')
```
- pandas import, read_table, plot() example

###Literal Constants

We use the values of literals literally, these values represent themselves and nothing else.

Type conversions:

- int(): Integers or whole numbers of any length like 2, 30, 1000
- float(): Floats or floating point numbers like 1.9, 30.01, 1e3 
- str(): String or sequence of characters like 'Hello',  '1 World', '&'
  - Single quote and double quotes
    - Either of the quote can be used to print a string
    - Spaces, tabs, comma etc. inside the quotes are preserved
  - Triple Quotes
    - Multi line strings can be specified by triple quotes (""" or ''')

### Comments 

Comments are preceded by a **#**, and are completely ignored by the python interpreter.

``` 
# Comments can be on their own line
print("Hello again!") # Comments can also be after line of code.
```

Comments are an incredibly useful way to keep track of what you are doing in
your code. Use comments to document what you do as much as possible, it will
pay off in the long run.

##Exercise - 1

- Print more strings
- Print numbers 
- Hint: does not need quotes
- Print a float with int() and integer with float() types
- Print multiple strings and numbers together
  - Hint 1: use comma as separator
  - Hint 2: use plus sign (+) to connect 
    - This gives error (or sum, when int1+int2) with numbers, how to solve this?
- Print a string with double quote
  - Example: 'this string appears with double quotes'

###Variables

- Using literal constants will become boring (what does Python do if you write everything on your own?)
- Variables are the instances for which different values can be assigned
  - Allow storing of information in your computer"s memory
- We need a method to access them
  - by giving them names (Identifiers)
- value assignment is done with single equals symbol `=`

####Rules:
- The identifiers are case sensitive 
  - myname and MyName are different
- must be unique (python will overwrite value of existing variable without warning you)
- The name cannot start with a number, or any special symbol (e.g. $, %, @, -, etc...) except for "_" (underscore), which is OK.
- The name cannot have any spaces or special characters (except for "-" (hyphen) and "_" (underscore))



####Conventions
- The name starts with a (usually lower case) letter
- Followed by letters, underscores or digits (name_1)

###String formatter

The string format operators allows formatting output of strings, substituting in values of variables

Previous example
```
print('Age of', name, 'is', age)
```
Pythonic way 1: 
```
print('Age of {} is {}'.format(name, age))
```
Pythonic way 2: 
```
print('Age of %s is %s' % (name, age))
```
There are several options with %:
- %s: string
- %d: decimal point number
- %f: float point number
- %.2f: float point number to 2 decimal places

##Exercise - 2

Assign any value to variable i, print and check the value
```
i = 10
```
Reassign a different value to i, print and check
```
i = 23
```
(You just overwrote the value of i, the last assigned value is the current value)

Assign multiple variables same values, print and check
```
a = b = c = 59
```
Assign multiple variables (a, b, c) different values
- Option - 1
```
a = 1
b = 2 
c = 3
```
- Option - 2
```
a, b, c = 1, 2, 3
```

###Operators and operands

Operators are functionality that do something and can be represented by the symbols such as + or special keywords
- Operators operate on data referred as operands, here the numbers and letters are operands and the symbols (+,* ...) are operators
```
4 + 6
```
```
5 * 8
```
```
'a' + 'b'
```
```
'5' + '3' # what do you expect here?
```

##Exercise - 3

Assign numerical values to x and y and do the following

```
x = 20
y = 98
```

Sum x and y by plus
```
x + y
```
Subtract y from x by minus
```
x - y
```
Multiply x and y
```
x * y
```
Multiply a string with y
```
"X" * y
```
Return x to the power of y
```
x**y
```
Divide x by y
```
x/y
```
Return remainder of x divided by y
```
x % y
```
Check if x is greater than y
```
x > y
```
Check if x is smaller than y
```
x < y
```
Check if x is less than or equal to 100
```
x <= 100
```
Check if y is greater than or equal to 5
```
y >= 100
```
Check if x is equal to y
```
x == y
```
Check if x is not equal to y
```
x != y
```

###Math operators and operands

We can use multiple operators together

Evaluation order is what high school taught us: BODMAS
- B: Brackets first
- O: Orders (i.e. Powers and Square Roots, etc.)
- DM: Division and Multiplication (left-to-right)
- AS: Addition and Subtraction (left-to-right)

- Division before multiplication and addition before subtraction
- However the order can be altered by using brackets, for example
```
4/2*3+1-5 = 2 but 4/2*(3+1-5) = -2
```

Use multiple operators
```
x+y*(y/x)
```

Operands can be over-written
- Solution – 1
  - Assign a value to variable a
  - Reassign/overwrite value of a as a * 3
```
a = 2
a = a * 3
a
```
- Solution – 2
  - Assign a value to variable a
  - Reassign/overwrite value of a as a * 3
```
a = 2
a *= 3
a
```

###Data structure - 1

Data Structures are containers that hold/store a collection of data/object together 
There are two built-in data structures that we will discuss here
- List (list): holds ordered collection of objects separated by comma
  - Objects are present in the given order any change in introduced
  - Lists are mutable: data can be added and removed
An empty list are created as
```
my_list = []
```
A list with values are created as
```
my_list = [1, 2, "a", "b"]
```

#### Aside - objects, errors, help(), and dir()
- pretty much everything in Python is an object
  - a package of information, with type dependent on value, and associated information (attributes) about that value/object, and standard set of operations (methods) available for the value/object
- __reading Python error messages__
  - create some commonly-seen errors - NameError (variable name typo), TypeError (can't perform operation with variable(s) of this type/these types e.g. str addition with int), IndexError, etc...
- use `help(x)` to see the documentation (if it exists) for `x`
- use `dir(y)` to see the available attributes and methods for `y`

##Exercise - 4

Print and check at each step
```
help(list)
```

Create a list with five items and follow the exercise
```
my_list = [1, 2, "C", 4, "E"]
```
Add/append an item
```
my_list.append("X")
```
Access the list item by index, which are the position of items (counted from 0)
Access the 1st item (square brackets to define the index)
```
my_list[0] 
```
Access the last item
```
my_list[-1]
```
Access the 4th item (?)
```
my_list[...]
```
Access items from position 2 to 4. Here 4 means item in the 5th position, last mentioned index is not accessed
```
my_list[1:4] 
```
Access items at the index 2 to the second last position (?)
```
```
Access items from the beginning to the position 4
```
mylist[:4]
```
Access items at the index 2 to the last position (?)
```
```
Insert an item in the 4th position
```
my_list.insert(3, "X")
```
Check the items in the list and find the number of items
```
len(my_list)
```
Remove "X" from the list. Check the length again
```
my_list.remove("X")
```
Remove an item from a position from any index (i=3)
```
my_list.pop(i)
```
Get maximum value in the list
```
max(my_list)
```
Get minimum value in the list (letters are considered larger than digits)
```
min(my_list)
```
Reverse items in the list
```
my_list.reverse()
```
Sort items of the list
```
my_list.sort()
```
Reverse the items again
```
```
Summed up the value of a list containing all the numerical items: sum(list_num)
```
list_num = [1, 2, 3, 4]
```
Convert a string into list
```
my_string = "convert string into list"
list(my_string)
```
Count the occurrence of an item
- hint-1: 
```
list("convert string into list").count("t")
```
- hint-2: 
```
new_list = list("convert string into list")
new_list.count("t")
```
Convert a string into list by splitting it by space
```
my_string.split("  ")
```
Get unique items of the list
```
set(new_list)
```
Note: Set is another data structute, with an unordered collection without duplicates Created as
```
my_set = set()
```
Dealing with two lists: define 2 lists with some items (list1 and list2)
```
```
Create a third list as list3
```
list3 = list1 + list2
```
Extend list1 by list2
```
list1.extend(list2)
```
Create a list with only unique items from the lists
```
set(list1).union(list2)
```
Find common items in the lists
```
set(list1).intersection(list2)
```

###Data structure - 2

Dictionary (dict): a list of key-value pairs where key can be any numbers or string and values can be any arbitrary python object

An empty dict is created as
```
my_dict = {}
```
or 
```
my_dict = dict()
```

A dictionary contains a set of key-value pairs, where a key and its value are separated by a colon (:)

```
my_dict = {"Key_1": "Val_1"}
```

keys must be unique (trying to create a second entry in the dict for a key will overwrite the existing value for that key)

####Aside: mutable vs non-mutable
Why did we say that you can only use strings and numbers as keys in a dict? These object types are _immutable_ - their value cannot be changed in place. Lists and dictionaries are _mutable_ - you can add, remove, and change their entries whenever you please. Dictionaries are designed to allow very fast lookup of information, and this design requires that the value of a key and therefore its location in memory can be relied upon not to change.  
If you need an immutable sequence of entries, you can use a _tuple_.
  
##Exercise - 5

Create a dictionary with key-value pairs
```
my_dict = {"name": "Khaleesi", "age": 20}
```
Access value by a key
```
my_dict["name"]
```
or 
```
my_dict.get("name")
```
Add more items to the dictionary
```
my_dict["occupation"] = "Queen"
```
Print all the items - note the order
```
my_dict
```
Print all the key-value pairs as list
```
my_dict.items()
```
Print all the keys of the dictionary as list
```
my_dict.keys()
```
Print all the values of the dictionary as list
```
my_dict.values()
```
Remove a key-value pair
```
my_dict.pop("age")
```
Check if a key is in the dict: "location" in my_dict and "age" in my_dict
```
```
Remove all the items from the dict
```
my_dict.clear()
```

###For Loops
Time for some real programming. The biggest motivation for researches to learn a programming language is the opportunity to automate repetitive tasks and analyses.

For loops define a set of steps that will be carried out for all items in a sequence. The items in the sequence will be taken one-at-a-time, and the loop performed, until there are no more items to process.

```
for season in ['Spring', 'Summer', 'Autumn', 'Winter']:
	print(season)
```
####Important Points
- syntax: whitespace, `:`, `for` statement and `in` operator
- the "loop variable" - `season` in the example above
  - stores the value aken from the sequence in the current iteration.
- "sequence" means list, dict, string, tuple, and more...
### if/else
As well as looping, the other key ingredient to programming automated processes is "flow control" i.e. executing different instructions depending on some detectable factor.

```
if weather == 'sunny':
	need_to_buy = 'sunblock'
else:
	need_to_buy = 'an umbrella'
print('Before I go on holiday, I need to buy', need_to_buy)
```
