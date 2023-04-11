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

# 4 Pillars of OOP
![image](https://user-images.githubusercontent.com/100339175/231120359-e146a0fa-4076-4c27-b203-d95c37f8f09d.png)

- Polymorphism 
- Inheritance
- Abstraction
- Encapsulation


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
- Inheritance allows us to define a class that inherits all the methods and properties from another class. 
- Parent class is the class being inherited from, also called base class. 
- Child class is the class that inherits from another class, also called derived class.
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
### Inheritance 2
- We cam use isinstance to check if one class is a subclass of the other.
```
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
print(isinstance(wizard1, Wizard)) #True, wizard1 is the subclass of Wizard
print(isinstance(wizard1, User)) #True, wizard1 is the subclass of user
print(isinstance(wizard1, Object)) #True, because Python is all object programming.
```

### Polymorphism
- Polymorphism defines the ability to take different forms. 
- Polymorphism in Python allows us to define methods in the child class with the same name as defined in their parent class.
```
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
archer1 = Archer("Robin", 1000)

def player_attack(char):
  char.attack()

player_attack(wizard1)
player_attack(archer1)

# Result: The same function gives a different output, because of polymorphism.
# attacking with power of 50
# Attacking with arrows, Left with 1000
```
- Another way of displaying we can use polymorphism to work.

```
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
archer1 = Archer("Robin", 1000)

for char in [wizard1, archer1]:
  char.attack()

#Result: Same Result as above
```
- polymorphism allows us to have many forms
- For example, we can even use the parent class method in the subclass
```
class User(): #Parent Class
  def sign_in(self):
    print('logged in')

  def attack(self):
    print('do nothing')

class Wizard(User): #Subclass
  def __init__(self, name, power):
    self.name = name
    self.power = power

  def attack(self):
    User.attack(self)
    print(f"attacking with power of {self.power}")

class Archer(User): #Subclass
  def __init__(self, name, num_arrows):
    self.name = name
    self.num_arrows = num_arrows

  def attack(self):
    print(f"Attacking with arrows, Left with {self.num_arrows}")

wizard1 = Wizard("Merlin", 50)
archer1 = Archer("Robin", 1000)

for char in [wizard1, archer1]:
  char.attack()
# Result
# do nothing
# attacking with power of 50
# Attacking with arrows, Left with 1000
```
- Polymorphism allows us to refine methods from derived classes such as archer and wizard.
- And object that instantiated can be behave in different ways and forms because of polymorphism.

### Exercise
https://replit.com/@aneagoie/inheritance-exercise

Solution: https://replit.com/@LightGamer1/inheritance-exercise?v=1


### Super()
- The super() function is used to give access to methods and properties of a parent or sibling class. 
- The super() function returns an object that represents the parent class.
```
class User(): #Parent Class
  def __init__(self, email):
    self.email = email
  
  def sign_in(self):
    print('logged in')

  def attack(self):
    print('do nothing')

class Wizard(User): #Subclass
  def __init__(self, name, power, email):
    super().__init__(email)
    self.name = name
    self.power = power

  def attack(self):
    User.attack(self)
    print(f"attacking with power of {self.power}")

class Archer(User): #Subclass
  def __init__(self, name, num_arrows):
    self.name = name
    self.num_arrows = num_arrows

  def attack(self):
    print(f"Attacking with arrows, Left with {self.num_arrows}")

wizard1 = Wizard("Merlin", 50, "wizard1@gmail.com")
archer1 = Archer("Robin", 1000)

print(wizard1.email)

#Result: wizard1@gmail.com
```

- Another example of super()
```
class Parent:
  def __init__(self, txt):
    self.message = txt

  def printmessage(self):
    print(self.message)

class Child(Parent):
  def __init__(self, txt):
    super().__init__(txt)

x = Child("Hello, and welcome!")

x.printmessage()
```

### Introspection
- introspection is the ability to determine the type of an object at runtime.
- It is one of Python's strengths. Everything in Python is an object and we can examine those objects. 
- Python ships with a few built-in functions and modules to help us.

Example
- if we add this dir(), we are able to see what this object has access to
```
print(dir(wizard1))
#Result
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'attack', 'email', 'name', 'power', 'sign_in']
```
- Note that: email, attack, name, power, sign_in are available

### Dunder Methods
- In Python, dunder methods are methods that allow instances of a class to interact with the built-in functions and operators of the language.
- Also known as "special methods"
- We are able to do some custom modify to these "special methods"

```
class Toy():
  def __init__(self, color, age):
    self.color = color
    self.age = age
    self.my_dict = {
      'name' : 'Yoyo',
      'has_pets': False
    }

  def __str__(self):
    return f"{self.color}"

  def __len__(self):
    return 5

  def __call__(self):
    return "yessss?"

  def __getitem__(self, i):
    return self.my_dict[i]

action_figure = Toy('red', 0)
print(action_figure.__str__())
print(str(action_figure))
print(len(action_figure))
print(action_figure())
print(action_figure['name'])

#Result"
# red
# red
# 5
# yessss?
# Yoyo
```

