# OOP

*"Everything in Python is an object"*

 **OOP** allows user to create *new data types*

## Class

```mermaid
graph TD;
    Class-->Data/Property;
    Class-->Function/Behavior;
```

Class is a blueprint that dictates how an object/function will act.

```
list() -- This is  class

l = list([1,2,3]) -- This is an object of the class
```

Class is written using **PASCAL**

    - HelloWorld -- *This is pascal*

### Object

Object is an instance of a class

### Example of OOP

Lets create a small **ATM** using OOP.


```
class Atm:

    # constructor 
    '''
    - All variables are created inside constructor
    - Constructor is a special function
        - It has a superpower --> It will automatically-execute unlike other functions
    '''
    def __init__(self):
        self.pin = ''
        self.balance = 0
        self.amount = 0
        # print('Auto execute')
        self.menu()
        

    def menu(self):
        user_input = input("""              
              How can I help you?
              1 : Press 1 to create PIN?
              2 : Press 2 to change PIN.
              3 : Press 3 to check balance
              4 : Press 4 to withdraw
              5 : Anything else to exit
              """)
        if user_input =='1':
            self.create_pin()
            # Create PIN
        elif user_input == '2':  
            self.change_pin()
            #change pin
        elif user_input == '3':
            self.check_balance()
            #check balance
        elif user_input == '4':
            self.withdrawl()
        # withdraw
        else:
            exit()

    def create_pin(self):
        user_pin = input('Enter your PIN')
        self.pin = user_pin

        user_balance = int(input('Enter balance'))
        self.balance = user_balance

        print("Code created successfully!")
        self.menu()

    def change_pin(self):
        old_pin = input("Enter old PIN")
        if old_pin == self.pin:
            new_pin = input("Enter new PIN")
            self.pin = new_pin
            print("PIN changed successful")
            self.menu()
        else:
            print("Can't change pin")
            self.menu()

    def check_balance(self):
        user_pin = input("Please enter your PIN")
        if user_pin == self.pin:
            print(f'The balance is {self.balance}')
        else:
            print("Wrong PIN")
        self.menu()
        
    def withdrawl(self):
        user_pin = input("Enter your PIN")
        if user_pin == self.pin:
            with_drawl = int(input("How much money would like to withdrawl"))
            if with_drawl >0:
                # balance = input("Blance you would like to withdraw")
                new_balance = self.balance - with_drawl
                print(f"Total balance is {new_balance}")
                self.balance = new_balance
            else:
                print("Your balance is 0")
        else:
            print("Incorrect credentials")
        self.menu()
```

## Methods vs functions

**Method** are functions that are written with *OOP* whereas functions that are independed and outside of a class. 

## Class Diagram

```mermaid
graph TD;
    Class-->Data/Variables/Attributes;
    Data/Variables/Attributes-->Method;

```

- **+** - Public

- **-** Private

## Magic Method *aka Dunder **Method*

Magic &rarr; Special &rarr; Super Power

- `__name__` &rarr; This is a method method
  - e.g. `__init__` &rarr; Constructor

### What are some true benefits of a constructor?

- True benefits is used to write *configuration related code*. 

- God is programmer &rarr; Earth is class &rarr; Humans are objects.
    
- Constructor purpose in this example would be to prevent humans from have the power of death.

## Self 

- Self is a *default* parameter in all functions in class. 

- Self allows methods to communicate with each other in OOP

- self &harr; object

#### Golden Rule of OOP

- Attributes and method can only be accessed by it's *object*. 
- It cannot communicate with each other. 

### `__str__ `

- Returns code in a class
### `__add__`

- Allows us to add

### `__sub__, __Multi__, __Div__`

- They all do their respective operations.

# Encapsulation

### Write OOP classes to handle the following scenarios:;

- A user can create and view 2D coordinates
- A user can find out the distance between 2 coordinates
- A user can find the distance of a coordinate from origin 
- A user can check if a point lies on a given line 
- A user can find the distance between a given 2D point and a given line

```
class Point:
    def __init__(self,x_coordinate, y_coordinate):
        self.x_coordinate = x_coordinate
        self.y_coordinate = y_coordinate

    def __str__ (self):
        return '< {}, {} >'.format(self.x_coordinate, self.y_coordinate)
    
    def eucliden_distance(self, other):
        return ((self.x_coordinate - other.y_coordinate)**2 + (self.y_coordinate - other.y_coordinate)**2)**0.5
    
    def distance_from_origin(self):
        return self.eucliden_distance(Point(0,0))
    
class LineClass:
    def __init__(self, A,B,C):
        self.A = A
        self.B = B
        self.C = C
    
    def __str__(self):
        return '{}x + {}y + {} = 0'.format(self.A, self.B, self.C)
    
    def point_on_line(line, point):
        if line.A*point.x_coordinate + line.B*point.y_coordinate + line.C == 0:
            return 'Lies on the line'
        else:
            return 'Does not lie on the line'
        
    def shortest_distance(line, point):
        return abs(line.A*point.x_coordinate + line.B*point.y_coordinate + line.C)/(line.A**2 + line.B**2)
```
## Reference Variable

Variable used to create an object contains reference of the object

- Refrence variables hold the objects
- We can create objects without reference variable as well
- An object can have multiple reference variable
- Assigning a new reference variable to an existing object does not create a new object

```mermaid
graph TD;
    A --> B;
    A -->  Memory-Address;
    B --> Memory-Address;
```

## Pass by reference

UDF functions in python are *mutable*


```
class Person:
    def __init__(self, name, gender):
        self.name = name
        self.gender = gender

def greet(person):
    print('Hi, my name is', person.name, 'and I am a', person.gender)
    print(id(person))
    p1 = Person('Batman', 'Male')
    return p1

p = Person('Batman', 'Male')
x = greet(p)
print(id(p))
print(x.name)
print(x.gender)
```
##  Encapsulation

**Instance Variable** - Instance variables are type of variables that have different values for each object.

- `__ name` will make a private variable 

- `__name` create a new variable in the memory therefor it can not be accessed outside the class

- ***"Nothing truly is private in python"***

- Always use `__` infront of each variable

### Purpose 
- Make variable private 
- Getter and Setter 

## Static vs Instance 

Instance variable is different for *each object* whereas static variable is *same for all objects.*

- Instance is inside the constructor whereas static is inside each method

## Class Relationships

- Aggregation
- Inheritance

## Class Relationship: Aggregation

```mermaid
classDiagram
    class Engine {
        +horsepower int
    }
    class Car {
        +make string
        +model string
        +engine Engine
        +car_details() string
    }

    Car o-- Engine : Aggregation
```

- Aggregation: This is a "has-a" relationship where one class contains a reference to another class. It represents a whole-part relationship, but both classes can exist independently.

- **Note**: Aggregation can’t be performed directly on private variables, as private members are meant to be accessed only within their own class.

```
class Engine:
    def __init__(self, horsepower):
        self.horsepower = horsepower

class Car:
    def __init__(self, make, model, engine):
        self.make = make
        self.model = model
        self.engine = engine  # Aggregation: Car "has-a" Engine

    def car_details(self):
        return f"{self.make} {self.model} with {self.engine.horsepower} HP engine"

engine = Engine(150)
car = Car("Toyota", "Corolla", engine)
print(car.car_details())  # Output: Toyota Corolla with 150 HP engine

```

## Inheritance and Polymophism


## Inheritance

Inheritance is a fundamental concept in OOP that allows one class (the child or derived class) to inherit attributes and methods from another class (the parent or base class).


### What gets inherited?

```mermaid
classDiagram
    class Animal {
        +make_sound() void
    }
    class Dog {
        +make_sound() void
    }
    class Cat {
        +make_sound() void
    }

    Animal <|-- Dog
    Animal <|-- Cat
```

- Attributes and Methods: The child class inherits all the attributes and methods from the parent class. However, the child class can override these methods or extend them if needed.

- Constructor (__init__ method): The constructor of the parent class is not automatically called in the child class. You need to use super() to call it explicitly if required.

```
class Parent:
    def __init__(self):
        self.parent_attribute = "This is a parent attribute."

    def show_message(self):
        return "This is a message from the parent class."

class Child(Parent):
    def __init__(self):
        super().__init__()  # Calling the parent constructor
        self.child_attribute = "This is a child attribute."

child_instance = Child()
print(child_instance.parent_attribute)  # Output: This is a parent attribute.
print(child_instance.show_message())    # Output: This is a message from the parent class.

```
- Public and Protected Members: The child class inherits all public and protected members of the parent class. Private members are not directly inherited but can be accessed using getter and setter methods if needed.

## Method Overriding 

Method Overriding occurs when a child class provides a specific implementation of a method that is already defined in its parent class. The overridden method in the child class should have the same name, return type, and parameters as the method in the parent class.


```
# Parent class
class Animal:
    def make_sound(self):
        return "Some generic animal sound"

# Child class
class Dog(Animal):
    # Overriding the make_sound method
    def make_sound(self):
        return "Woof!"

# Child class
class Cat(Animal):
    # Overriding the make_sound method
    def make_sound(self):
        return "Meow!"

# Using the classes
animal = Animal()
dog = Dog()
cat = Cat()

print(animal.make_sound())  # Output: Some generic animal sound
print(dog.make_sound())     # Output: Woof!
print(cat.make_sound())     # Output: Meow!
```

## Super Keyword

### `super` Keyword in Python

The `super` keyword in Python is used to call a method from the parent class. It is commonly used to call the parent class’s constructor or to access methods that have been overridden in a child class.

---

### Using `super` in Python

#### 1. Calling the Parent Class Constructor
When you create a constructor (`__init__`) in a child class and still want to call the parent class’s constructor, you use `super()`.

```python
class Animal:
    def __init__(self, species):
        self.species = species
        print(f"Animal created: {self.species}")

class Dog(Animal):
    def __init__(self, name):
        # Call the parent class constructor
        super().__init__("Dog")
        self.name = name
        print(f"Dog created: {self.name}")

my_dog = Dog("Buddy")
# Output:
# Animal created: Dog
# Dog created: Buddy
```

#### 2. Calling Overridden Methods

If a child class overrides a method from the parent class, you can still call the parent class’s version of the method using super().

```
class Animal:
    def make_sound(self):
        return "Some generic animal sound"

class Dog(Animal):
    def make_sound(self):
        # Call the parent class's make_sound method
        parent_sound = super().make_sound()
        return f"{parent_sound} and Woof!"

dog = Dog()
print(dog.make_sound())  # Output: Some generic animal sound and Woof!

```

### How super Works

- Order of Resolution: The super() function uses the method resolution order (MRO) to determine the parent class to call. This is especially useful in complex inheritance hierarchies.
- Multiple Inheritance: In cases of multiple inheritance, super() helps to ensure that the parent class is called in the correct order, avoiding repetition.

### Benefits of Using super

-Avoid Hardcoding Parent Class Names: super() makes your code more maintainable and flexible.
- Support for Multiple Inheritance: super() properly handles the method resolution order in the case of multiple inheritance.

---

## Types of Inheritance 

```mermaid
classDiagram
    class A {
        +method()
    }

    class B {
        +method()
    }

    class C {
        +method()
    }

    class D {
        +method()
    }

    class E {
        +method()
    }

    %% Single Inheritance
    A <|-- B : Single Inheritance

    %% Multilevel Inheritance
    B <|-- C : Multilevel Inheritance

    %% Hierarchical Inheritance
    A <|-- D : Hierarchical Inheritance
    A <|-- E : Hierarchical Inheritance

    %% Multiple Inheritance
    B <|-- C : Multiple Inheritance
    D <|-- C : Multiple Inheritance
```

- `Single Inheritance:` A single child class (B) inherits from a single parent class (A).
- `Multilevel Inheritance:` A chain of inheritance where class C inherits from class B, which in turn inherits from class A.
- `Hierarchical Inheritance:` Multiple child classes (D and E) inherit from the same parent class (A).
- `Multiple Inheritance:` A single child class (C) inherits from multiple parent classes (B and D).

## Polymorphism in Python

Polymorphism is a core concept of Object-Oriented Programming that allows objects of different classes to be treated as objects of a common superclass. It enables the same interface to be used for different underlying forms (data types).

---

### Key Points
1. **Polymorphism** allows methods in different classes to have the same name but different implementations.
2. **Dynamic Typing** in Python enables polymorphism, allowing a function to use objects of different types as long as they have the required method or attribute.

---

### Types of Polymorphism
1. **Method Overloading** (Not natively supported in Python): Having multiple methods in the same class with the same name but different parameters.
2. **Method Overriding**: Redefining a method in the child class that is already defined in the parent class.
3. **Operator Overloading**: Using the same operator for different operations, depending on the operands.

---

### Example: Method Overriding
```python
class Animal:
    def make_sound(self):
        return "Some generic animal sound"

class Dog(Animal):
    def make_sound(self):
        return "Woof!"

class Cat(Animal):
    def make_sound(self):
        return "Meow!"

# Using Polymorphism
animals = [Dog(), Cat(), Animal()]

for animal in animals:
    print(animal.make_sound())
# Output:
# Woof!
# Meow!
# Some generic animal sound
```

## Abstraction in Python

### What is Abstraction?
Abstraction is one of the fundamental concepts of Object-Oriented Programming (OOP) that is used to hide the complexity of a system and only expose the necessary features. It focuses on what an object does rather than how it does it.

In Python, abstraction can be achieved using:
1. **Abstract Classes**
2. **Abstract Methods**

---

### Abstract Classes
An **abstract class** is a class that cannot be instantiated and is designed to be a blueprint for other classes. It can have abstract methods (methods declared but not implemented) as well as concrete methods (implemented methods).

To create an abstract class in Python, you use the `abc` module (Abstract Base Classes).

```python
from abc import ABC, abstractmethod

# Abstract class
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

# Concrete class
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

# Creating an object of the concrete class
rect = Rectangle(10, 5)
print("Area:", rect.area())          # Output: Area: 50
print("Perimeter:", rect.perimeter())  # Output: Perimeter: 30
```

### Key Points

- `Cannot Instantiate Abstract Class:` You cannot create an object of an abstract class directly.
`shape = Shape()  # This will raise an error`

- `Must Implement Abstract Methods:` Any concrete subclass must implement all the abstract methods defined in the abstract class.

### Why Use Abstraction?

 -   `Simplifies Complex Systems:` By showing only the essential details, abstraction reduces complexity and improves the readability of the code.
 -   `Increases Flexibility:` You can define a common interface for a group of related classes.
 -   `Enforces Implementation:` Abstract methods ensure that subclasses implement the methods defined in the abstract class.
  
### Use Cases of Abstraction

 -   `Frameworks and Libraries:` Abstraction is commonly used in frameworks and libraries to provide a clear and simple interface for users.
 -   `Real-World Example:` Consider a vehicle class that provides an abstract method start_engine(). Different types of vehicles (e.g., cars, bikes, planes) will implement start_engine() differently, but users don't need to worry about those details.