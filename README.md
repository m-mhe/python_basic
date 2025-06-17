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
active = False # This is a variable with boolean data.
if active:
    print("Already active")
else:
    active = True
    print("Activated")
```

    Activated
    

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

    The following list element will get deleted: 3
    




    [1, 'itemTwo', 'itemThree', 'itemFour', 'itemFive']


