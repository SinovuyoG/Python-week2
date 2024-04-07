# Python-week2

# ANATOMY OF CLASSES-:

The __init__() Function

To understand the meaning of classes we have to understand the built-in __init__() function.

All classes have a function called __init__(), which is always executed when the class is being initiated.

Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created:

class Person:

  def __init__(self, name, age):
  
    self.name = name
    
    self.age = age

p1 = Person("John", 36)

print(p1.name)

print(p1.age)

Note: The __init__() function is called automatically every time the class is being used to create a new object.

Note: The self parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.

It does not have to be named self , you can call it whatever you like, but it has to be the first parameter of any function in the class

Modify Object Properties

You can modify properties on objects like this:

Example

Set the age of p1 to 40:

p1.age = 40

Delete Object Properties

You can delete properties on objects by using the del keyword:

Example

Delete the age property from the p1 object:

del p1.age


Delete Objects

You can delete objects by using the del keyword:

Example

Delete the p1 object:

del p1

The pass Statement

class definitions cannot be empty, but if you for some reason have a class definition with no content, put in the pass statement to avoid getting an error.

Example

class Person:
  pass
  


# Instance Attributes vs. Static Attributes in Python Classes

# Instance Attributes:

Definition: Attributes specific to each instance of a class.

Scope: Belong to individual objects created from the class.

Initialization: Typically defined within methods, like __init__, or added dynamically.

Uniqueness: Hold data unique to each object.

Access: Accessed and modified using dot notation (object.attribute).
Example:

class Car:

    def __init__(self, color, model):
    
        self.color = color  # Instance attribute
        
        self.model = model  # Instance attribute

car1 = Car("Red", "Toyota")

car2 = Car("Blue", "Honda")

print(car1.color)  # Output: Red

print(car2.color)  # Output: Blue


# Static Attributes:

Definition: Attributes shared among all instances of a class.

Scope: Defined within the class but outside any methods.

Commonality: Common to all instances, changes reflect across all.

Access: Accessed using the class name or through any instance.

Example:

class Car:
    wheels = 4  # Static attribute

car1 = Car()

car2 = Car()

print(car1.wheels)  # Output: 4

print(car2.wheels)  # Output: 4

Car.wheels = 6  # Modifying static attribute

print(car1.wheels)  # Output: 6

print(car2.wheels)  # Output: 6


Instance Attributes: Unique to each object, defined within methods, accessed with dot notation.

Static Attributes: Shared among all instances, defined outside methods, accessed using class name.

# Python Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.

Parent class is the class being inherited from, also called base class.

Child class is the class that inherits from another class, also called derived class.
