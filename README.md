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

# Python Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.

Parent class is the class being inherited from, also called base class.

Child class is the class that inherits from another class, also called derived class.
