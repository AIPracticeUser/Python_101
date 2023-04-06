# Python Basic 2

## Tenary Operator

- Condition_if_true if condition else condition_if_else
Example
```
is_friend = True
can_message = "message allowed" if is_friend else "not allowed to message"

#Result: message allowed
```
## For Loop
```
for item in (1,2,3,4,5)
  for x in ('a', 'b', 'c')
    print(item, x)
    
Result:
1a
1b
1c
2a
.
.
5c
```
## Iterables
```
user = {
  'name': 'Golem',
  'age' : 5006,
  'can_swim': False
  
for item in user.items():
  print(item)
  
#result: 
#('name', 'Golem')
#('age', 5006)
#('can_swim', False)

for item in user.values():
  print(item)

#result:
# Golem
# 5006
# False

for item in user.keys():
  print(item)
  
#result:
# name
# age
# can_swim

for key, value in user.items():
  print(key, value)

# result:
# name Golem
# age 5006
# can_swim False

```

### Range
```

#Ascending +2 steps
for _ in range(0, 10, 2):
  print(_)

#Result
#0
#2
#4
#6
#8

#Descending
for _ in range(10, 0, -1):
  print(_)
  
#Result
#10
#9
#8
#7
#6
#5
#4
#3
#2
#1

for _ in range(0, 10, 2):
  print(list(range(10)))

#Result:
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

```

### enumerate()
```
for char in enumerate("Hello"):
  print(char)
  
#Result
#(0, 'H')
#(1, 'e')
#(2, 'l')
#(3, 'l')
#(4, 'o')


for i,char in enumerate("Hello"):
  print(i,char)
  
#Result
#0 H
#1 e
#2 l
#3 l
#4 o

for i,char in enumerate([1,2,3]):
  print(i,char)
  
#Result
#0 1
#1 2
#2 3


for i,char in enumerate((1,2,3)):
  print(i,char)
#0 1
#1 2
#2 3

for i,char in enumerate(list(range(100))):
  if char == 50:
    print(f"the index is {i}")

# the index is 50
```
### Finding duplicates exercise
https://replit.com/@LightGamer1/Find-Duplicates?v=1

### First GUI exercise
https://replit.com/@LightGamer1/GUI-exercise?v=1

### DocStrings
```
def test(a):
  '''
  Info: this function tests and prints para
  '''
  print(a)

print(test.__doc__)

#Result:  Info: this function tests and prints para
```
### Clean Code
```
# clean code
def is_even(num):
  if num % 2 == 0:
    return True
  elif num % 2 != 0:
    return False

print(is_even(51))
# We can clean the codes to have better readability

def is_even(num):
  if num % 2 == 0:
    return True
  return False

print(is_even(51))
#This works the same , but we can clean it even better

def is_even(num):
  return num % 2 == 0
  
print(is_even(51))
```

### *args **kwargs
- *args = positional arguments
```
def super_func(*args):
  print(*args)
  return sum(args)

super_func(1,2,3,4,5)

# This return the parameters
Result: 1 2 3 4 5
```

```
def super_func(*args):
  print(args)
  return sum(args)

print(super_func(1,2,3,4,5))

# This actually returns the tuple
Result: (1, 2, 3, 4, 5)
#15
```

- **kwargs = keyword arguments
```
def super_func(name, *args, i='hi', **kwargs):
  total = 0
  for items in kwargs.values():
    total += items
  return sum(args) + total

print(super_func('Andy', 1,2,3,4,5, num1=5, num2=10))

#Rule: params , *args, default parameter, **kwargs 
#Need to follow the above rule for function params
#Result: 30
```

### Exercise 2
- Find the highest even number in the list
https://replit.com/@LightGamer1/Highest-Even-Number?v=1

### Scopes
- What variables do I have access to?


