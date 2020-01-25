# Quick References For Python

## Basic

### Commenting
```python
# This is a single line comment

"""
This is
a multi-line
comment 
"""
```

### Printing
```python
# Printing a custom string
print("This is so cool")

# Printing only variables
a = 50
b = "people"
print(a) # prints >> 50
print(b) # prints >> people

# String formatting
c = 15.4923421
print("There are %d %s in the room"%(a,b)) # prints >> There are 50 people in the room
print("He has %.4f grams of gold"%c) #prints >> He has 15.4923 grams of gold
print("He has %.1f grams of gold"%c) #prints >> He has 15.5 grams of gold
```

### Getting user input

```python
A = input("Enter a number")
print(A*2) # prints >> 1212 (if the number entered was 12)

# Need to convert to int to use it as integer variable
A = int(A)
print(A*2) # Now prints >> 24 (if A = 12)

# You can also write as 
A = int(input("Enter a number"))
```

### Pass argument through terminal while you run the script

chatBot.py
```python
from sys import argv

# pass argument while you run the script
script,name,age = argv  # NOTE that the first argumment is by default the script name.
age = int(age)

# showing how intelegent your chatbot is !! :-p
print("\nHi %s !! All I know about you is that you are %d years old\n\n"%(name,age))
```
run the code through terminal and parse your arguments in the following way
```shell
$ python3 chatBot.py robot 10
```
output you get is 
```shell
Hi robot !! All I know about you is that you are 10 years old
```


### conditional statements
Conditional statements are used frequently in coding. we use one of the following operator`== , <= , < , > , >=` to write a conditional statement comparing the LHS and RHS expression. For example
```python
a = 3
print(4 == 3) # is 4 equal to 3 ?? Nope so it will print false
print(7 >= a) # is 7 greater than/equal to 3 ?? yes so it will print true
print(7 <= 7) # This will print true
```
you can perform boolean operations (or combinations of boolean operations) like AND, OR, NOT on conditional statements. For example
```python
b = 12
print( (4<b) or (7 < 4)) # (true OR false) thus this will print true
print( not(b < 6)) # This will print true
```

### if, elif, else statements
We use if, elif and else to run a perticular set of instructions only if some condition is true. It basically helps our code to have some conditionaly varying behaviour.

```python
if true:
  print("string 1")
else:
  print("string 2")
# Output of above code block is >> string 1

if false:
  print("string 1")
else:
  print("string 2")
# Output of above code block is >> string 2

# An example of how we can use conditional statements with if, elif ,else 
password = "XyWq1"
user_input = intput("Enter password")

if user_input == password:
  print("Access granted !!")
else :
  print("SORRY! AND BYE!")
```

### Lists in python
As the name suggests we can enlist different values of same/different data type into a python list.
```python
# Creating a list
ShoppingList = ["bag","shoes","water bottle"] # This is how you define a list list1 = [val1, val2 , ...]

# To add new elements to the list
ShopppingList.append("T-Shirt")

# To remove an element at the ith index
ShoppingList.pop(0) # This will remove "bag" from the list

# To remove an element by value
ShoppingList.remove("shoes") 
```

### Dictionaries
```python

# Creating a dictionary
info = {'name':'kaustubh', 'city':'Vadodara'} # We write as key:value pairs in the dictionary

# Can you search a word(key) by using its meaning(value) in the dictionary ?? Nope so even in python 
# This is how we search in a value .... using the key
print(info['city']) # Prints Vadodara

# Adding a key:value pair to a dictionary
info['hobby'] = 'music'

# Editing value for a key in the dictionary
info['city'] = 'Mumbai' # This will change 'city':'Vadodara pair to 'city':'Mumbai' pair

# Removing a key value pair
del info['city']
```

### Loops  
We use loops to perform certain task multiple times. 

while loop
```python
i = 0
while i <10:
  i += 1
  print(i)

# Basically the loop of instructions goes on and on till the while condition is true
```
for loop
```python

for i in range(10):
  print(i)
# Prints 0,1,.... till 9
```

### Functions
We basically write a set of code inside a function and simply `call` the function when we want those lines of to be executed. With functions we have two cool things we can do ! we can pass some specific values to a function (called arguments) which can be used by the function and if needed the function can also return a value back so it can be used in the remaining code. There are four major types of functions 

1. Functions which neither take argument nor return any argument
```python

def function1():
  print("Hi! I am a function that does not take any argument nor return any value")

# How do we use it in the main code ??
function1()

```
2. Functions which take in arguments but do not return any value
```python

def add(a,b):
  print("Sum of %r and %r is %r"%(a,,b,a+b))
  
# Using the function in main code
add(10,12) # prints >> Sum of 10 and 12 is 22
```

3. Function which does not take any argument but returns some value
```python

def getPI():
  PI = 3.14
  return 3.14

# using in the main code
pi = getPI()
print("Value of pi using the function is %r"%pi)
```

4. Function which takes input as well as returns some value
```python

def add(a,b):
  c = a+b
  return c

# Using in main function
a = 10
b = 12
c = add(a,b)
print("Sum of %r and %r is %r"%(a,b,c))
```


