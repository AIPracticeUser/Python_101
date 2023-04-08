# OOP - Object Oriented Programming
- Object-oriented programming (OOP) is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior.
- 
### Structure of OOP

- Classes are user-defined data types that act as the blueprint for individual objects, attributes and methods.
- Objects are instances of a class created with specifically defined data. Objects can correspond to real-world objects or an abstract entity. When class is defined initially, the description is the only object that is defined.
- Methods are functions that are defined inside a class that describe the behaviors of an object. Each method contained in class definitions starts with a reference to an instance object. Additionally, the subroutines contained in an object are called instance methods. Programmers use methods for reusability or keeping functionality encapsulated inside one object at a time.
- Attributes are defined in the class template and represent the state of an object. Objects will have data stored in the attributes field. Class attributes belong to the class itself.

![image](https://user-images.githubusercontent.com/100339175/230718303-ed7177e1-3c08-4d85-a0bf-5b8d74b702c8.png)


### What are the main principles of OOP?
- Object-oriented programming is based on the following principles:

- Encapsulation. This principle states that all important information is contained inside an object and only select information is exposed. The implementation and state of each object are privately held inside a defined class. Other objects do not have access to this class or the authority to make changes. They are only able to call a list of public functions or methods. This characteristic of data hiding provides greater program security and avoids unintended data corruption.
- Abstraction. Objects only reveal internal mechanisms that are relevant for the use of other objects, hiding any unnecessary implementation code. The derived class can have its functionality extended. This concept can help developers more easily make additional changes or additions over time.
- Inheritance. Classes can reuse code from other classes. Relationships and subclasses between objects can be assigned, enabling developers to reuse common logic while still maintaining a unique hierarchy. This property of OOP forces a more thorough data analysis, reduces development time and ensures a higher level of accuracy.
- Polymorphism. Objects are designed to share behaviors and they can take on more than one form. The program will determine which meaning or usage is necessary for each execution of that object from a parent class, reducing the need to duplicate code. A child class is then created, which extends the functionality of the parent class. Polymorphism allows different types of objects to pass through the same interface.

### What are the benefits of OOP?
- Benefits of OOP include:
- Modularity. Encapsulation enables objects to be self-contained, making troubleshooting and collaborative development easier.
- Reusability. Code can be reused through inheritance, meaning a team does not have to write the same code multiple times.
- Productivity. Programmers can construct new programs quicker through the use of multiple libraries and reusable code.
- Easily upgradable and scalable. Programmers can implement system functionalities independently.
Interface descriptions. Descriptions of external systems are simple, due to message passing techniques that are used for objects communication.
- Security. Using encapsulation and abstraction, complex code is hidden, software maintenance is easier and internet protocols are protected.
- Flexibility. Polymorphism enables a single function to adapt to the class it is placed in. Different objects can also pass through the same interface.

### Example
```
class BigObject:
  pass

obj1 = BigObject()
print(type(None))
print(type(True))
print(type(5))
print(type(5.5))
print(type([]))
print(type(()))
print(type({}))
print(type(obj1))

#Result:
<class 'NoneType'>
<class 'bool'>
<class 'int'>
<class 'float'>
<class 'list'>
<class 'tuple'>
<class 'dict'>
<class '__main__.BigObject'>
```

### Example 2
```
class PlayerCharacter:
  #Constructor
  def __init__(self, name, age):
    #attributes
    self.name = name
    self.age = age

  #method
  def run(self):
    print('run')
    return 'done'

#instaniated
player1 = PlayerCharacter('Cindy', 44)
player2 = PlayerCharacter('Tom', 21)
player2.attack = 50

print(player1.name, player1.age)
print(player1.run())
print(player2.name, player2.age)
print(player2.attack)

#Result:
# Cindy 44
# run
# done
# Tom 21
# 50
```

### Attributes and Methods
- Continued from previous example, there is a help function
```
help(player1)

#Result
Help on PlayerCharacter in module __main_
_ object:

class PlayerCharacter(builtins.object)
 |  PlayerCharacter(name, age)
 |  
 |  Methods defined here:
 |  
 |  __init__(self, name, age)
 |      Initialize self.  See help(type(s
elf)) for accurate signature.
 |  
 |  run(self)
 |      #method
 |  
 |  -------------------------------------
---------------------------------
 |  Data descriptors defined here:
 |  
 |  __dict__
 |      dictionary for instance variables
 (if defined)
 |  
 |  __weakref__
 |      list of weak references to the ob
ject (if defined)
```
### Class Object Attribute
- A class attribute is a variable that belongs to a certain class, and not a particular object.
- Every instance of this class shares the same variable.
- These attributes are usually defined outside the __init__ constructor
```
class PlayerCharacter:
  #Class object Attribute
  membership = True
  def __init__(self, name, age):
    #attributes
    if (PlayerCharacter.membership):
      self.name = name
      self.age = age
  
  #method
  def shout(self):
    print(f'My name is {self.name}')
    print(f'I am {self.age} years old')

#instaniated
player1 = PlayerCharacter('Cindy', 44)
player1.shout()

#Result:
My name is Cindy
I am 44 years old
```

