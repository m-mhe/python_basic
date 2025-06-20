# Hello World


```python
# This is how we write comments in python
print("Hello World") #'print()' is a function that gives output of object inside it's parenthesis.
```

    Hello World


# Data Types

### There are four main data types in python

#### 1. String


```python
name = "momin hosan emon" #This is a variable with string data.
print(f"My name is {name.title()}")
```

    My name is Momin Hosan Emon


#### 2. Boolean


```python
active = None # This is a variable with boolean data. "None" is null data type in python
if active:
    print("Already active")
elif active == None:
    print("----Error Occurred----")
else:
    active = True
    print("Activated")
```

    ----Error Occurred----


#### 3. Integer


```python
print(24564) # All whole positive & negative numbers are integer
```

    24564


#### 4. Float


```python
print(665.546548765468986) # All fraction numbers are float
```

    665.546548765469



```python
print(type(active)) # Shows the data type of a variable.
```

    <class 'bool'>


# String Methods



```python
print(name.upper()) # Shows all the letter in upper case.
```

    MOMIN HOSAN EMON



```python
print(name.lower()) # Shows all the letter in lower case.
```

    momin hosan emon



```python
print(name.title()) # Shows first letter of a word in upper case.
```

    Momin Hosan Emon



```python
print(name.count('m')) # Counts how many 'm' are in this string.
```

    3



```python
print(name.replace('e','i')) #Every 'e' letters will get replaced by the letter 'i' but it doesn't change the original variable.
name # The variable is not changed
```

    momin hosan imon





    'momin hosan emon'



# Variable


```python
varName ="Hello world" #This is a simple variable
```

# String Concatenation


```python
concatenateString = varName+" My name is "+name.title()
print(concatenateString)
```

    Hello world My name is Momin Hosan Emon


# f String


```python
print(f"{varName} My name is {name.title()}") # f string used to make inline string concatenations.
```

    Hello world My name is Momin Hosan Emon


# List


```python
listName = ['itemOne', 'itemTwo', 3, 'itemFour']
listName
```




    ['itemOne', 'itemTwo', 3, 'itemFour']



### List Methods


```python
listName[2] # To access a list element by their index.
```




    'itemThree'




```python
listName[-1] # To access list element of the list.
```




    'itemFive'



##### Slicing:


```python
print(listName[0:3])
print(listName[1:]) # From index one to last
print(listName[:3]) # From first to index 3
listName[0:-1] #From 0 to index number 2
```

    ['itemOne', 'itemTwo', 3]
    ['itemTwo', 3, 'itemFour']
    ['itemOne', 'itemTwo', 3]





    ['itemOne', 'itemTwo', 3]



##### Adding elements to a list:


```python
listName.append('itemFive')
listName
```




    ['itemOne', 'itemTwo', 3, 'itemFour', 'itemFive']




```python
listName.insert(2, 'itemThree')
listName
```




    ['itemOne', 'itemTwo', 'itemThree', 3, 'itemFour', 'itemFive']




```python
listName[0] = 1
listName
```




    [1, 'itemTwo', 'itemThree', 'itemFour', 'itemFive']



##### Nested List:


```python
nestedList = [listName, listName[1:]] # This is how we can add list and keep in a nested list variable, nested list are kind a 2 dimantional array of C/C++.
print(nestedList)
```

    [[1, 'itemTwo', 'itemThree', 'itemFour', 'itemFive'], ['itemTwo', 'itemThree', 'itemFour', 'itemFive']]


##### Deleting elements from a list:


```python
print(f"The following list element will get deleted: {listName.pop(3)}") # Or if we do not give any index 'object.pop()' then it will delete the last item from the list.
listName
```

    The following list element will get deleted: itemFour





    [1, 'itemTwo', 'itemThree', 'itemFive']




```python
country = listName.copy() #This is how we can copy a list. This method is same for dictionaries in python.
country.append("Iran")
country.append("Israil")
country.insert(2, "USA")
print(country)
country.remove("Israil") #This is how we can delete an item by it's value.
print(country)
del country[2] # Same as pop() method, but it doesn't return deleted value.
print(country)
```

    ['itemOne', 'itemTwo', 'USA', 3, 'itemFour', 'Iran', 'Israil']
    ['itemOne', 'itemTwo', 'USA', 3, 'itemFour', 'Iran']
    ['itemOne', 'itemTwo', 3, 'itemFour', 'Iran']


##### List Sorting:


```python
nums = [5,7,3,9,1,4,0,6,8,2]

nums.sort()
print(nums)

nums.sort(reverse = True) #For sorting in reverse order
print(nums)

alpha = ['H','E','A','C','F','G','J','K','B','D','I']

alpha.sort()
print(alpha)

alpha.sort(reverse = True) #For sorting in reverse order
print(alpha)
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
    ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K']
    ['K', 'J', 'I', 'H', 'G', 'F', 'E', 'D', 'C', 'B', 'A']


##### To update an element from list:


```python
person = ['Imon', 'Karim', 'Jubair']

person[0] = 'Emon'
person[2] = 'Rafiq'
print(person)
```

    ['Emon', 'Karim', 'Rafiq']


# Dictionary


```python
newMap = {'keyOne':'valueOne','keyTwo':'valueOne','keyThree':'value68','keyFour':'valueFour','keyFive':'valueFive','keyOne':'value68',}#in dart we call it map
newMap
```




    {'keyOne': 'value68',
     'keyTwo': 'valueOne',
     'keyThree': 'value68',
     'keyFour': 'valueFour',
     'keyFive': 'valueFive'}



### Accessing Item From Dictionary:


```python
print(newMap.keys())
print(str(newMap.values())+"\n") # We have done type conversion using "str(object_that_we_want_to_convert_in_string)".

for key, value in newMap.items():
    print(f"{key.title()}: {value.title()}")
```

    dict_keys(['keyOne', 'keyTwo', 'keyThree', 'keyFour', 'keyFive'])
    dict_values(['value68', 'valueOne', 'value68', 'valueFour', 'valueFive'])
    
    Keyone: Value68
    Keytwo: Valueone
    Keythree: Value68
    Keyfour: Valuefour
    Keyfive: Valuefive


### To add or edit:


```python
newMap['keyOne']="value1" # Editing with key name
print(newMap)
newMap.update({'key2':'value2'}) # Or we can add or edit like this
print(newMap)
newMap['key6']='value6' # We can also add new item pair to dictionary like this
print(newMap)
```

    {'keyOne': 'value1', 'keyTwo': 'valueOne', 'keyThree': 'value68', 'keyFour': 'valueFour', 'keyFive': 'valueFive'}
    {'keyOne': 'value1', 'keyTwo': 'valueOne', 'keyThree': 'value68', 'keyFour': 'valueFour', 'keyFive': 'valueFive', 'key2': 'value2'}
    {'keyOne': 'value1', 'keyTwo': 'valueOne', 'keyThree': 'value68', 'keyFour': 'valueFour', 'keyFive': 'valueFive', 'key2': 'value2', 'key6': 'value6'}


### To Delete:


```python
del newMap['key6'] # Deleting by accessing key.
print(newMap)
newMap.clear() # Deleting all items, same for list.
print(newMap)
```

    {'keyOne': 'value1', 'keyTwo': 'valueOne', 'keyThree': 'value68', 'keyFour': 'valueFour', 'keyFive': 'valueFive', 'key2': 'value2'}
    {}


# Function


```python
def add(a,b):
    return a+b

print(add(6,4))
```

    10


### Build-in Functions


```python
listName = [45,5454,454,4588,41,212,65]
mapName = {464:246544564,44:76,478:9999}
setName={'A','C','d','F','u','c','K','A'} # Same as list but cant't contain duplicate items in it.

print("\n# Iterable item numbers")
print(len(listName))
print(len(mapName))
print(len(steName))

print("\n# Maximum")
print(max(mapName))
print(max(mapName.items())) # also works for list and other iterable objects of python.
print(max(mapName.keys()))
print(max(mapName.values()))

print("\n# Minimum")
print(min(mapName))
print(min(mapName.items())) # also works for list and other iterable objects of python.
print(min(mapName.keys()))
print(min(mapName.values()))

print("\n# Sorted list")
# setName.sort() it won't work.
listName.sort()
print(listName)
## mapName.sort() it also won't work.
## print(mapName)

print("\n# Objetc Types")
print(type(listName))
print(type(mapName))
print(type(steName))

print("\n# Range Function")
for i in range(0,100,5): # 0 to 100 in interval of 5
    print(i)
```

    
    # Iterable item numbers
    7
    3
    7
    
    # Maximum
    478
    (478, 9999)
    478
    246544564
    
    # Minimum
    44
    (44, 76)
    44
    76
    
    # Sorted list
    [41, 45, 65, 212, 454, 4588, 5454]
    
    # Objetc Types
    <class 'list'>
    <class 'dict'>
    <class 'set'>
    
    # Range Function
    0
    5
    10
    15
    20
    25
    30
    35
    40
    45
    50
    55
    60
    65
    70
    75
    80
    85
    90
    95


# Module


```python
import os as lol # Here os is a module.

print(lol.getcwd()) # Checking current directory

print(lol.listdir()) # It gives us all file and folder name under cwd (Current Working Directory)

lol.makedirs("this_folder_is_created_with_python_os_module")

print(lol.listdir()) # It gives us all file and folder name under cwd (Current Working Directory)
```

    /home/mmhe/ds_codebase/python_basic
    ['.ipynb_checkpoints', '.git', 'part_one.ipynb']
    ['this_folder_is_created_with_python_os_module', '.ipynb_checkpoints', '.git', 'part_one.ipynb']

