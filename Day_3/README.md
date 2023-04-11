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

### Exercise 3
- Find the oldest cat
```
import random
#Given the below class:
class Cat:
    species = 'mammal'
    def __init__(self, name, age):
        self.name = name
        self.age = age


# 1 Instantiate the Cat object with 3 cats
cat = []
for i in range(3):
 cat.append(Cat("cat" + str(i+1), random.randint(1,20)))
 print(f"Cat {i+1} age: {cat[i].age}")


# 2 Create a function that finds the oldest cat
def oldest_cat(cat_list):
  max = 0
  for n in range(len(cat_list)):
    if cat_list[n].age > max:
      max = cat[n].age
  return max


# 3 Print out: "The oldest cat is x years old.". x will be the oldest cat age by using the function in #2
oldest_cat_age = oldest_cat(cat)
print(f"The oldest cat is {oldest_cat_age} years old")
```
https://replit.com/@LightGamer1/OOP-Exercise-Cat-1?v=1

### @classmethod
```
#OOP
class PlayerCharacter:
  membership = True
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def minus_things(self):
    return "omg"
  
  @classmethod
  def adding_things(cls, num1, num2):
    return num1 + num2

player1 = PlayerCharacter('Tom', 20)

print(player1.minus_things())
print(PlayerCharacter.adding_things(2,3))  #with classmethod, the class does not need to be instantated

#Result:
#omg
#5

```
### Using the @classmethod to instatited
```
#OOP
class PlayerCharacter:
  membership = True
  def __init__(self, name, age):
    self.name = name
    self.age = age

  # def minus_things(self):
  #   return "omg"
  
  @classmethod
  def adding_things(cls, num1, num2):
    return cls("Teddy", num1 + num2)

player1 = PlayerCharacter('Tom', 20)

# print(player1.minus_things())
player3 = PlayerCharacter.adding_things(2,3)
print(player3.age)
```

### @staticmethod
- Using staticmethod does not have access to the class parameters
- Using classmethod have access to class parameters
```
#OOP
class PlayerCharacter:
  membership = True
  def __init__(self, name, age):
    self.name = name
    self.age = age

  # def minus_things(self):
  #   return "omg"
  
  @classmethod
  def adding_things(cls, num1, num2):
    return cls("Teddy", num1 + num2)

  @staticmethod
  def adding_thing2(num1, num2):
    return num1 + num2

player1 = PlayerCharacter('Tom', 20)

# print(player1.minus_things())
player1 = PlayerCharacter.adding_things(2,3)
print(player1.age)
player2 = PlayerCharacter.adding_thing2(4,5)
print(player2)
```
- both @classmethod and @staticmethod will not be encountered often

### Encapsulation
- Encapsulation refers to the bundling of attributes and methods inside a single class. 
- It prevents outer classes from accessing and changing attributes and methods of a class. 

### Abstraction 
- Abstraction in python is defined as a process of handling complexity by hiding unnecessary information from the user.
- Example
```
print(len((1,2,3,1))
#Result: 4
# We do not need to know how len function is implement, only need to know the method of calling it
```
### Private and Public Variables
```
class PlayerCharacter:
  def __init__(self, name, age):
    self._name = name   #The underline before the name of the variable is just a convention to tell the users that this is private property
    self._age = age

  def run(self):
    print('run')

  def speak(self):
    print(f"My name is {self._name}, and I am {self._age} years old")

player1 = PlayerCharacter('Steven', 100)

player1.speak()
```

### Inheritance
```
# With inheritance,  sublass can both execute the sign-in functiom at same time.
class User(): #Parent Class
  def sign_in(self):
    print('logged in')

class Wizard(User): #Subclass
  def __init__(self, name, power):
    self.name = name
    self.power = power

  def attack(self):
    print(f"attacking with power of {self.power}")

class Archer(User): #Subclass
  def __init__(self, name, num_arrows):
    self.name = name
    self.num_arrows = num_arrows

  def attack(self):
    print(f"Attacking with arrows, Left with {self.num_arrows}")

wizard1 = Wizard("Merlin", 50)
archer1 = Archer("Robin", 100)
wizard1.sign_in()
wizard1.attack()
archer1.sign_in()
archer1.attack()
```


