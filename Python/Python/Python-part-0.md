[Python](../Python.md) / Python part 0

# Python part 0

 

Variable declaration

doesn’t need datatype specification

```python
x = 5
x = True
x = 'char'
```

to find the datatype of a variable we can use `type` method

```python
print(type(x))
#<class, 'str'>
```

## Variables

Declaration doesn’t need datatype

- python is case sensitive

```python
age = 20
fName = 'John'
isGood = True
```

accepting input

```python
name = input("what is your name: ")
```

datatype conversion

```python
name = input("what is your name? ")
boy = input("what year were you born? ")
print("hello " + name + ", you are " + str(2024 - int(boy)) + " years old")
```

to find the datatype of a variable we can use `type` method

```python
print(type(x))
#<class, 'str'>
```

## to store list of elements

### List

```python
names = ["John", "Bob", "Katy", "Mosh"]
print(names[0]) #John
print(names[-2]) #Katy
names[0] = "Jon"
print(names[0:3]) #['Jon', 'Bob', 'Katy']

```

List object methods

```python
numbers = [1, 2, 3, 4, ,5]

#to add new entry/element at the end
numbers.append(6)
print(numbers) #[1, 2, 3, 4, ,5, 6]

#to add new entry/element at a specific index
numbers.insert(-1, 6) #(index, element)
print(numbers) #[1, 2, 3, 4, ,5 , 6]

#to remove an element
numbers.remove(1)
print(numbers) #[2, 3, 4, ,5, 6]

#to remove all elements
numbers.clear()
print(numbers) #[]

#to check for an elements
print(1 in numbers) #False

#to find number of elements
print(numbers.len()) #5

```

### Tuples

are immutable lists

```python
numbers = (1, 2, 3)
numbers[0] = 4 #error
```

there are only two methods `.count()` and `.index()`

```python
#to count the number of occurences of an element
numbers = (1, 2, 3, 3)
print(numbers.count(3)) #2

#to find an element and return the index
numbers = (1, 2, 3, 3)
print(numbers.index(3)) #2
```

### Set

a list that can’t hold duplicated element

```python
names = {"John", "Bob", "Katy", "Mosh"}
print(names[0]) #{"John", "Bob", "Katy", "Mosh"}

```

Set methods

```python
names.add("Bob")
print(names) #{"John", "Bob", "Katy", "Mosh"}

names = {"John", "Bob", "Katy", "Mosh"}
names.add("Mkenzi")
print(names) #{"John", "Bob", "Katy", "Mosh", "Mkenzi"}
```

### Dictionary

to store a key, value pair list of elements

```python
studentInfo = {
	'name': 'hanna', 'age': 12, 'sec': 'B', 
	'skills': ['java', 'javaScript', 'python']
}
```

to access specific values

```python
print(studentInfo['skills'])
#['java', 'javaScript', 'python']
```

### Datatype casting

datatype conversion

```python
name = input("what is your name? ")
boy = input("what year were you born? ")
print("hello " + name + ", you are " + str(2024 - int(boy)) + " years old")
```

## Flow control

### For loop

```python
numbers = [1, 2, 3, 4, ,5]

for item in numbers:
	print(item)
#1
#2
#3
#4
#5
```

- **Range function**
    
    to generate a sequence of numbers, returns an object
    
    ```python
    numbers = range(5)
    print(numbers) #range(0, 5)
    
    for number in numbers:
    	print(number)
    #1
    #2
    #3
    #4
    #5
    
    #specific starting and end points [srart, end)
    numbers1 = range(1, 5) 
    
    for number in numbers1:
    	print(number)
    #1
    #2
    #3
    #4
    
    ```
    

```python
for item in range(1, 6):
	print(item)
#1
#2
#3
#4
#5
```

```python
#to have both index and values we can use enumerate()
names = {"John", "Bob", "Katy", "Mosh"}
for index, value in enumerate(names):
	print(str(index) + ' ' + str(value))
```

### If-else

```python
weight = float(input("Enter weight: "))
unit = input("(K)g or (L)bs: ")
if unit.upper() == "K":
    weight *= 2.204
    print(weight)
elif unit.upper():
    weight /= 2.204
    print(weight)
else:
    print("Invalid unit")
```

## Function

```python
def greet():
	print('hello world!')

greet()

def greet():
	print('hello world!')
	
def greett(name):
	print(f'hello {name}')
	
greett('hanna')

def greet3(name, age, last_name = 'kebede'):
	print(f'hello {name} age: {age} last Name: {last_name}')
	
greet3('hanna', 12, 'bekele')
greet3('hanna', age = 50) #this is right
```

- argument types
    
    positional argument
    
    ```python
    greet('hanna', 50) #this is right
    ```
    
    key word argument
    
    ```python
    greet(age = 50) #this is right
    ```
    
    default argument
    
    ```python
    def greet3(name, age, last_name = 'kebede'):
    	print(f'hello {name} age: {age} last Name: {last_name}')
    
    greet('hanna', 50) #this is right
    ```
    
- Rules in parameter passing
    - key word argument can’t come first in argument passing
        
        ```python
        greet('hanna', age = 50) #this is right
        greet(age = 50, 'hanna') #this will cause error
        ```
        
    - non default argument must come first
    - default argument must come last