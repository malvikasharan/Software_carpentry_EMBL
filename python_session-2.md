##Python session - 2

##Aim of this session: 

Control flow: automating repeated boring tasks using loops rather than actively commanding Python to do stuffs (print, add etc.)

Control-flow allows Python to take a decision and do different things depending on different situations using if/else or for loops

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

```
temperature = input()
if temperature > 25:
    print("Nice weather!")
elif temperature < 25:
    print("Winter is coming!")
else:
    print("The temperature is 25 degree.")
```


###For loop
```
shopping = ['bread', 'potatoes', 'eggs', 'flour', 'rubber duck', 'pizza', 'milk']
for item in shopping:
  print(item)
```
