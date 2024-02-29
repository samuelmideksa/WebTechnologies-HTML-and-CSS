[Python](../Python.md) / Python part 1

# Python part 1

### Lambda function

```python
''' syntax
lambda parameter: expression
'''

# to squre a list of numbers
numbers = [3, 4, 34, 5, 6, 17]
square_value = []

def squre_list(list_elements):
    for number in list_elements:
        square_value.append(number*number)
    print(square_value)

squre_list(numbers)

square = lambda number: number*number

even_odd = lambda number: 'even number' if number % 2==0 else 'odd number'
print(square(5))
print(even_odd(5))

''' output
[9, 16, 1156, 25, 36, 289]
25
odd number
'''
```

### Map function

to map function with iterable

```python
''' syntax
map(function, iterables)
'''

# to squre a list of numbers
numbers = [3, 4, 34, 5, 6, 17]
square_value = []

print(list(map(lambda number: number*number, numbers)))

```

### Filter function

filter an iterable and returns the values with True

```python
''' syntax
filter(function with bool return type, iterables)
'''

# to get even numbers from list of numbers
numbers = [3, 4, 34, 5, 6, 17]
square_value = []

even_values = filter(lambda number: True if number % 2 == 0 else False, numbers)
print(list(even_values))

'''output
[4, 34, 6]
'''
```

# object Oriented Programming

**Principles of Object-Oriented Programming (OOP) in Python**

Object-Oriented Programming (OOP) is a paradigm that structures software design around objects, which encapsulate data and behavior.

1. **Encapsulation**:
Encapsulation involves bundling data and methods that operate on the data into a single unit, i.e., an object. This shields the data from direct access and manipulation, allowing controlled interactions through methods.
    
    ```python
    class Car:
        def __init__(self, make, model):
            self.make = make
            self.model = model
    
        def display_info(self):
            print(f"Car: {self.make} {self.model}")
    
    my_car = Car("Toyota", "Camry")
    my_car.display_info()  # Output: Car: Toyota Camry
    
    ```
    
2. **Inheritance**:
Inheritance enables a class (subclass) to inherit properties and behaviors from another class (superclass). This promotes code reusability and hierarchical organization.
    
    ```python
    class Vehicle:
        def __init__(self, make, model):
            self.make = make
            self.model = model
    
        def display_info(self):
            print(f"Vehicle: {self.make} {self.model}")
    
    class Car(Vehicle):
        def __init__(self, make, model, year):
            super().__init__(make, model)
            self.year = year
    
    my_car = Car("Toyota", "Camry", 2022)
    my_car.display_info()  # Output: Vehicle: Toyota Camry
    
    ```
    
3. **Polymorphism**:
Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables methods to behave differently based on the object they are called on.
    
    ```python
    class Animal:
        def sound(self):
            pass
    
    class Dog(Animal):
        def sound(self):
            return "Woof!"
    
    class Cat(Animal):
        def sound(self):
            return "Meow!"
    
    def make_sound(animal):
        print(animal.sound())
    
    dog = Dog()
    cat = Cat()
    
    make_sound(dog)  # Output: Woof!
    make_sound(cat)  # Output: Meow!
    
    ```
    
4. **Abstraction**:
Abstraction focuses on hiding the complexities of implementation and exposing only essential features. It allows defining interfaces with concrete implementations deferred to subclasses.
    
    ```python
    from abc import ABC, abstractmethod
    
    class Shape(ABC):
        @abstractmethod
        def area(self):
            pass
    
    class Square(Shape):
        def __init__(self, side):
            self.side = side
    
        def area(self):
            return self.side ** 2
    
    class Circle(Shape):
        def __init__(self, radius):
            self.radius = radius
    
        def area(self):
            return 3.14 * self.radius ** 2
    
    square = Square(5)
    circle = Circle(3)
    
    print(square.area())  # Output: 25
    print(circle.area())  # Output: 28.26
    
    ```