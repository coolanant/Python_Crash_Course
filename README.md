# Python_Crash_Course

### 1. [Basic Python Syntax](https://github.com/coolanant/Python_Crash_Course/blob/master/Basic_Syntax.ipynb)

```.py
#1. Variables
x = 1           # int
y = 2.5         # float
name = 'Anant'   # str
is_cool = True  # bool

# Multiple assignment
x, y, name, is_cool = (1, 2.5, 'Anant', True)

# Basic math
a = x + y

# Casting
x = str(x)
y = int(y)
z = float(y)

print(type(z), z)
# <class 'float'> 2.0

#2. Strings
print('str'+str(y))
name='anant'
age=21
print('hi. My name is {name} and I am {age}'.format(name=name,age=age))
print(f'hi. My name is {name} and I am {age}')
str2
hi. My name is anant and I am 21
hi. My name is anant and I am 21
In [25]:
print(name.capitalize())
print(name.upper())
print(name.lower())
print(name.swapcase())
print(len(name))
print(name.replace('anant','anu'))
print(name.count('a'))
print(name.startswith('hello'))
print(name.endswith('t'))
print(name.split())
print(name.find('n'))
print(name.isalnum())
print(name.isalpha())
print(name.isnumeric())

#3. List
# Create list
numbers = [1, 2, 3, 4, 5]
fruits = ['Apples', 'Oranges', 'Grapes', 'Pears']

# Use a constructor
numbers2 = list((1, 2, 3, 4, 5))

# Get a value
print(fruits[1])

# Get length
print(len(fruits))

# Append to list
fruits.append('Mangos')

# Remove from list
fruits.remove('Grapes')

# Insert into position
fruits.insert(2, 'Strawberries')

# Change value
fruits[0] = 'Blueberries'

# Remove with pop
fruits.pop(2)

# Reverse list
fruits.reverse()

# Sort list
fruits.sort()

# Reverse sort
fruits.sort(reverse=True)

print(fruits)

# 4. Tuple
# A Tuple is a collection which is ordered and unchangeable. Allows duplicate members.

# Create tuple
fruits = ('Apples', 'Oranges', 'Grapes')

# Using a constructor
fruits2 = tuple(('Apples', 'Oranges', 'Grapes'))

# Single value needs trailing comma
fruits2 = ('Apples',)

# Get value
print(fruits[1])

# Can't change value
# fruits[0] = 'Pears'

# Delete tuple
del fruits2

# Get length
print(len(fruits))

# 5. Sets
# A Set is a collection which is unordered and unindexed. 
# No duplicate members.

# Create set
fruits_set = {'Apples', 'Oranges', 'Mango'}

# Check if in set
print('Apples' in fruits_set)

# Add to set
fruits_set.add('Grape')

# Remove from set
fruits_set.remove('Grape')

# Add duplicate
fruits_set.add('Apples')

# Clear set
# fruits_set.clear()

# Delete
# del fruits_set

print(fruits_set)

# 6. Dictionary
# A Dictionary is a collection which is unordered, changeable and indexed. No duplicate members.

# Create dict
person = {
    'first_name': 'Anu',
    'last_name': 'Rung',
    'age': 20
}

# Use constructor
# person2 = dict(first_name='Anant', last_name='Rungta')

# Get value
print(person['first_name'])
print(person.get('last_name'))

# Add key/value
person['phone'] = '123-456-789'

# Get dict keys
print(person.keys())

# Get dict items
print(person.items())

# Copy dict
person2 = person.copy()
person2['city'] = 'Delhi'

# Remove item
del(person['age'])
person.pop('phone')

# Clear
person.clear()

# Get length
print(len(person2))

# List of dict
people = [
    {'name': 'A', 'age': 10},
    {'name': 'B', 'age': 20}
]

print(people[1]['name'])

dict_keys(['first_name', 'last_name', 'age', 'phone'])
dict_items([('first_name', 'Anu'), ('last_name', 'Rung'), ('age', 20), ('phone', '123-456-789')])

# 7. Functions
def sayHello(name='Sam'):
    print(f'Hello {name}')

# Return values
def getSum(num1, num2):
    total = num1 + num2
    return total

sayHello()
print(getSum(1,2.1))

# 8. Lambda Functions
# A lambda function is a small anonymous function.
# A lambda function can take any number of arguments, but can only have one expression. Very similar to JS arrow functions

getSum = lambda num1, num2: num1 + num2

print(getSum(10, 3))

# 9. Conditionals
x = 21
y = 20

# 1. Comparison Operators (==, !=, >, <, >=, <=) - Used to compare values

# Simple if
if x > y:
  print(f'{x} is greater than {y}')

# If/else
if x > y:
  print(f'{x} is greater than {y}')
else:
  print(f'{y} is greater than {x}')  

# elif
if x > y:
  print(f'{x} is greater than {y}')
elif x == y:
  print(f'{x} is equal to {y}')  
else:
  print(f'{y} is greater than {x}')  

# Nested if
if x > 2:
  if x <= 10:
    print(f'{x} is greater than 2 and less than or equal to 10')
    

# 2. Logical operators (and, or, not) - Used to combine conditional statements

# and
if x > 2 and x <= 10:
    print(f'{x} is greater than 2 and less than or equal to 10')

# or
if x > 2 or x <= 10:
    print(f'{x} is greater than 2 or less than or equal to 10')

# not
if not(x == y):
  print(f'{x} is not equal to {y}')


# 3. Membership Operators (not, not in) - Membership operators are used to test if a sequence is presented in an object

numbers = [1,2,3,4,5]

#  in
if 3 in numbers:
  print(x in numbers)

# not in
if x not in numbers:
  print(x not in numbers)

# 4. Identity Operators (is, is not) - Compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:

# is
if x is y:
  print(x is y)

# is not
if x is not y:
  print(x is not y)
21 is greater than 20
21 is greater than 20
21 is greater than 20
21 is greater than 2 or less than or equal to 10
21 is not equal to 20
False
True
True
In [54]:
# 10. Lopps
In [56]:
# A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

people = ['John', 'Paul', 'Sara', 'Susan']

# Simple for loop
for person in people:
  print(f'Current Person: {person}')

# Break
for person in people:
  if person == 'Sara':
    break
  print(f'Current Person: {person}')

# Continue
for person in people:
  if person == 'Sara':
    continue
  print(f'Current Person: {person}')

# range
for i in range(len(people)):
  print(people[i])

for i in range(0, 11):
  print(f'Number: {i}')

# While loops execute a set of statements as long as a condition is true.
count = 0
while count < 10:
  print(f'Count: {count}')
  count += 1

# 11. Modules
# ! pip install camelcase
# A module is basically a file containing a set of functions to include in your application. There are core python modules, modules you can install using the pip package manager (including Django) as well as custom modules

# Core modules
import datetime
from datetime import date
import time
from time import time

# today = datetime.date.today()
today = date.today()
timestamp = time()
print(today,timestamp)

# # Pip module
# from camelcase import CamelCase
# c = CamelCase()
# # print(c.hump('hello there world'))
2020-02-23 1582436157.0655324
In [71]:
# 12. Classes
In [7]:
# A class is like a blueprint for creating objects. An object has properties and methods(functions) associated with it. Almost everything in Python is an object

# Create class
class User:
  # Constructor
  def __init__(self, name, email, age):
    self.name = name
    self.email = email
    self.age = age
    
  def greeting(self):
    return f'My name is {self.name} and I am {self.age}'

  def has_birthday(self):
    self.age += 1


# Extend class
class Customer(User):
  # Constructor
  def __init__(self, name, email, age):
    self.name = name
    self.email = email
    self.age = age
    self.balance = 0

  def set_balance(self, balance):
    self.balance = balance

  def greeting(self):
    return f'My name is {self.name} and I am {self.age} and my balance is {self.balance}'

#  Init user object
anu = User('anu rung', 'annu@gmail.com', 22)
# Init customer object
karan = Customer('karan', 'karan@yahoo.com', 20)

karan.set_balance(500)
print(karan.greeting())

anu.has_birthday()
print(anu.greeting())
My name is karan and I am 20 and my balance is 500
My name is anu rung and I am 23


#13. Files
# Python has functions for creating, reading, updating, and deleting files.

# Open a file
myFile = open('myfile.txt', 'w')

# Get some info
print('Name: ', myFile.name)
print('Is Closed : ', myFile.closed)
print('Opening Mode: ', myFile.mode)

# Write to file
myFile.write('Wow')
myFile.write(' Any Text')
myFile.close()

# Append to file
myFile = open('myfile.txt', 'a')
myFile.write(' Hi')
myFile.close()

# Read from file
myFile = open('myfile.txt', 'r+')
text = myFile.read(100)
print(text)

# 14. JSON API
# JSON is commonly used with data APIS. Here how we can parse JSON into a Python dictionary

import json

#  Sample JSON
userJSON = '{"first_name": "Anu", "last_name": "Rung", "age": 20}'

# Parse to dict
user = json.loads(userJSON)

# print(user)
# print(user['first_name'])

car = {'make': 'Ford', 'model': 'Mustang', 'year': 1970}

carJSON = json.dumps(car)

print(carJSON)
{"make": "Ford", "model": "Mustang", "year": 1970}
# Eception handling
import sys
def calculate_expenditure(list_of_expenditure):
    total=0
    try:
        for expenditure in list_of_expenditure:
            total+=expenditure
        print("Total:",total)
        avg=total/num_values
        print("Average:",avg)
    except ZeroDivisionError:
        print("Divide by Zero error")
    except:
         print(f'Error: {sys.exc_info()[1]}')

list_of_values=[100,200,300,"400",500]
num_values=5
calculate_expenditure(list_of_values)
Error: unsupported operand type(s) for +=: 'int' and 'str'


```

2. [Anaconda Official Video Tutorials](https://anaconda.cloud/)
