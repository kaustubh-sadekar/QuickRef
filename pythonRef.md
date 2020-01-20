# Quick References For Python

## Basic

**Commenting**
```python
# This is a single line comment

"""
This is
a multi-line
comment 
"""
```

**Printing**
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

**Getting user input**

```python
A = input("Enter a number")
print(A*2) # prints >> 1212 (if the number entered was 12)

# Need to convert to int to use it as integer variable
A = int(A)
print(A*2) # Now prints >> 24 (if A = 12)

# You can also write as 
A = int(input("Enter a number"))
```

**Pass argument through terminal while you run the script**

code1.py  
