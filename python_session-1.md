#Python session - 1

##Aim of this session: 

Learn the basics (what is? how to?)

###Classic beginning with "Hello World!"

- Run Python (Type ‘python’ + click run button)
- Print something
```
print(“Hello World!”)
```

###Literal Constants

We use the values of literals literally, these values represent themselves and nothing else.

- int(): Integers or whole numbers of any length like 2, 30, 1000
- float(): Floats or floating point numbers like 1.9, 30.01, 1e3 
- str(): String or sequence of characters like “Hello”,  “1 World”, “&”
  - Single quote and double quotes
    - Either of the quote can be used to print a string
    - Spaces, tabs, comma etc. inside the quotes are preserved
  - Triple Quotes
    - Multi line strings can be specified by triple quotes (‘’’ or “””)

##Excercise - 1

- Print more strings
- Print numbers 
- Hint: does not need quotes
- Print a float with int() and integer with float() types
- Print multiple strings and numbers together
  - Hint 1: use comma as separator
  - Hint 2: use plus sign (+) to connect 
    - gives error (or sum, when int1+int2) with numbers, how to solve this?
- Print a string with double quote
  - Example: “this string appears with double quotes”

###Variables

- Using literal constants will become boring (what does Python do if you write everything on my own?
- Variables are the instances for which different values can be assigned
  - Allow storing of information in your computer’s memory
- We need a method to access them by giving them names (Identifiers)

####Rules:
- The identifiers are case sensitive 
  - myname and MyName are different
- The name starts with a letter or alphabet
- Followed by letters, underscores or digits (name_1)

###String formatter

The string format operators allows formatting output of an ordered strings

- Previous example
```
print(“Age of”, name, “is”, age)
```
- Pythonic way 1: 
```
print(“Age of {} is {}”.format(name, age))
```
- Pythonic way 2: 
```
print(“Age of %s is %s” % (name, age))
```
- There are several options with %:
- %s: string
- %d: decimal point number
- %f: float point number
- %.2f: float point number to 2 decimal places

##Excercise - 2

- Assign any value to variable i, print and check the value
```
i = 10
```
- Reassign a different value to i, print and check
```
i = 23
```
  - You just overwrote the value of i, the last assigned value is the current value
- Assign multiple variables same values, print and check
```
a = b = c = 59
```
- Assign multiple variables (a, b, c) different values
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

###Opertaors and operands

- Operators are functionality that do something and can be represented by the symbols such as + or special keywords
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

##Exercise - 3

Assign numerical values to x and y and do the following

```
x = 20
y = 98
```

- Sum x and y by plus
```
x + y
```
- Subtract y from x by minus
```
x - y
```
- Multiply x and y
```
x * y
```
- Multiply a string with y
```
‘X’ * y
```
- Return x to the power of y
```
x**y
```
- Divide x by y
```
x/y
```
- Return remainder of x divided by y
```
x % y
```
- Check if x is greater than y
```
x > y
```
- Check if x is smaller than y
```
x < y
```
- Check if x is less than or equal to 100
```
x <= 100
```
- Check if y is greater than or equal to 5
```
y >= 100
```
- Check if x is equal to y
```
x == y
```
- Check if x is not equal to y
```
x != y
```

###Math operators and operands

We can use multiple operators together
- Evaluation order is what high school taught us: BODMAS

- B: Brackets first
- O: Orders (i.e. Powers and Square Roots, etc.)
- DM: Division and Multiplication (left-to-right)
- AS: Addition and Subtraction (left-to-right)

- Division before multiplication and addition before subtraction
- However the order can be altered by using brackets, for example
```
4/2*3+1-5 = 2 but 4/2*(3+1-5) = -2
```

- Use multiple operators
```
x+y*y/x)
```

- Operands can be over-written
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

- Data Structures are containers that hold/store a collection of data/object together 
- There are two built-in data structures that we will discuss here
  - List (list): holds ordered collection of objects separated by comma
    - Objects are present in the given order any change in introduced
    - Lists are mutable: data can be added and removed
- An empty list are created as
```
my_list = []
```
- A list with values are created as
```
my_list = [1, 2, ‘a’, ‘b’]
```

##Exercise - 4

- print and check at each step
```
help(list)
```

- create a list with five items and follow the exercise
```
my_list = [1, 2, ‘C’, 4, ‘E’]
```
- Add/append an item
```
my_list.append(‘X’)
```
- Access the list item by index, which are the position of items (counted from 0)
- Access the 1st item (square brackets to define the index)
```
my_list[0] 
```
- Access the last item
```
my_list[-1]
```
- Access the 4th item (?)
```
my_list[...]
```
- Access items from position 2 to 4. Here 4 means item in the 5th position, last mentioned index is not accessed
```
my_list[1:4] 
```
- Access items at the index 2 to the second last position (?)
```
```
- Access items from the beginning to the position 4
```
mylist[:4]
```
- Access items at the index 2 to the last position (?)
```
```
- Insert an item in the 4th position
```
my_list.insert(3, ‘X’)
```
- Check the items in the list and find the number of items
```
len(my_list)
```
- Remove ‘X’ from the list. Check the length again
```
my_list.remove(‘X’)
```
- Remove an item from a position from any index (i=3)
```
my_list.pop([i])
```
- Get maximum value in the list
```
max(my_list)
```
- Get minimum value in the list (letters are considered larger than digits)
```
min(my_list)
```
- Reverse items in the list
```
my_list.reverse()
```
- Sort items of the list
```
sorted(my_list)
```
- Reverse the items again
```
```
- Summed up the value of a list containing all the numerical items: sum(list_num)
```
list_num = [1, 2, 3, 4]
```
- Convert a string into list
```
my_string = ‘convert string into list’
list(my_string)
```
- Count the occurrence of an item
- hint-1: 
```
list(‘convert string into list’).count(‘t’)
```
- hint-2: 
```
new_list = list(‘convert string into list’)
new_list.count(‘t’)
```
- Convert a string into list by splitting it by space
```
my_string.split(‘  ’)
```
- Get unique items of the list
```
set(new_list)
```
Note: Set is another data structute, with an unordered collection without duplicates Created as
```
my_set = set()
```
- Dealing with two lists: define 2 lists with some items (list1 and list2)
```
```
- Create a third list as list3
```
list3 = list1 + list2
```
- Extend list1 by list2
```
list1.extend(list2)
```
- Create a list with only unique items from the lists
```
set(list1).union(list2)
```
- Find common items in the lists
```
set(list1).intersection(list2)
```

###Data structure - 2

- Dictionary (dict): a list of key-value pairs where key can be any numbers or strings and values can be any arbitrary python object
- An empty dict is created as
```
my_dict = {}
```
or 
```
my_dict()
```
- Key and value are separated by a colon (:)
- A list with key-value pairs are created as
```
my_dict = {‘Key_1’: ‘Val_1’}
```
  
##Excercise - 5

- Create a dictionary with key-value pairs
```
my_dict = {‘name’ : ‘Khaleesi’, ‘age’ : 20}
```
- Access value by a key
```
my_dict[‘name’]
```
or 
```
my_dict.get(‘name’)
```
- Add more items to the dictionary
```
my_dict[‘occupation’] = ‘Queen’
```
- Print all the items
```
my_dict
```
- Print all the key-value pairs as list
```
my_dict.items()
```
- Print all the keys of the dictionary as list
```
my_dict.keys()
```
- Print all the values of the dictionary as list
```
my_dict.values()
```
- Remove a key-value pair
```
my_dict.pop(‘age’)
```
- Remove the last key-value pair
```
my_dict.popitem()
```
- Check if a key is in the dict: ‘location’ in my_dict and ‘age’ in my_dict
```
```
- Remove all the items from the dict
```
my_dict.clear()
```
